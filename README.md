# luisponcho 
proyectos escolares y de más,
aprendiendo actualmente c++,
queriendo aprender muchos más lenguajes 

# Dist/github-snake.svg
# II dist/github-snake-dark.svg?palette=github-dark
# III dist/bylickilabs-Snake.svg?palette=github-dark&color_snake=red&color_dots=#000000F;#CDAD00;#EEC900;#FFD700;#FFD700;
# IV dist/bylickilabs-Snake.svg?palette=github-dark&color_snake=white&color_dots=#000000F;#5E5E5E;#787878;#919191;#BDBDBD;

            
      - ejecutar: estado de git

      - nombre: cambios push
        usos: ad-m/github-push-action@master
        con:
          github_token: ${{ secretos.GITHUB_TOKEN }}
          rama: maestro
          fuerza: verdadera

      - usos: crazy-max/ghaction-github-pages@v3.1.0
        con:
          target_branch: salida
          build_dir: dist
        entorno:
          GITHUB_TOKEN: ${{ secretos.GITHUB_TOKEN }}
