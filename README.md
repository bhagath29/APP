# APPHUB
import pygame
import sys

# Initialize pygame
pygame.init()

# Constants
SCREEN_WIDTH, SCREEN_HEIGHT = 400, 400
YELLOW = (255, 255, 0)
BLACK = (0, 0, 0)
RADIUS = 100

# Create a window
screen = pygame.display.set_mode((SCREEN_WIDTH, SCREEN_HEIGHT))
pygame.display.set_caption("AppHub")

# Main loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Clear the screen
    screen.fill(BLACK)

    # Draw a yellow circle in the center
    pygame.draw.circle(screen, YELLOW, (SCREEN_WIDTH // 2, SCREEN_HEIGHT // 2), RADIUS)

    # Update the display
    pygame.display.flip()

# Quit pygame
pygame.quit()
sys.exit()
