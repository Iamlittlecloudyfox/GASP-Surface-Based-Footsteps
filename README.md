# GASP-Surface-Based-Footsteps
This repository contains assets you can easily implement surface-based footsteps with in GASP for UE5.8. I watched some tutorials on YouTube, but I decided to make my own system. It is very fast and easy to make.

# Setup

1. Change your in-game files with these ones from the repository (paths should be exactly the same). Add GaspFoleySys folder with its content to the root of your project (Content).
2. Go to Project Settings and search for `surface`. You'll find textboxes for different surface types (if you want to fix BPF's errors add `Concrete` and `Wood` surface types here).
3. Go to your character's BP (For CMS and Mover logic is almost the same. I'll show how to implement it on the Mover one), search for the function called `On_MovementModeChanged_PostFinalize`.

    Connect `skeletal mesh` to `AC Foley Events` component as shown on the screenshot:
   <img width="858" height="367" alt="{9134186C-5FD3-403A-B8B9-CBC6715D3C4E}" src="https://github.com/user-attachments/assets/f92812db-da95-4e24-96fa-e2e4d21ca5b5" />
    <img width="823" height="413" alt="{B867628E-7FFD-42C6-A38A-5FB131997E31}" src="https://github.com/user-attachments/assets/49b56457-ef01-44a6-b958-956be8020a5f" />
    <img width="618" height="375" alt="{1CDEAC0D-CD33-469D-BAE9-64C1E6956B0A}" src="https://github.com/user-attachments/assets/f13cd155-65e1-4b15-b5a3-1bc264de48e5" />

That's it! Now your GASP character's footsteps should depend on the surface. If you want to add more surfaces - manipulate with Foley Audio Banks in the Audio directory. My template is shown in `BPF_GetSide`. 

