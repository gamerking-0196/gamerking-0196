import pygame
import sys

# Pygame başlat
pygame.init()

# Oyun alanı boyutları
width = 800
height = 600

# Ekran yüzeyini oluştur
screen = pygame.display.set_mode((width, height))
pygame.display.set_caption("Merhaba Dünya Oyunu")

# Ana oyun döngüsü
while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    # Ekranı temizle
    screen.fill((0, 0, 0))  # Siyah renk

    # Metni ekrana çiz
    font = pygame.font.Font(None, 36)
    text = font.render("Merhaba, Dünya!", True, (255, 255, 255))  # Beyaz renk
    text_rect = text.get_rect(center=(width // 2, height // 2))
    screen.blit(text, text_rect)

    # Ekranı güncelle
    pygame.display.flip()
