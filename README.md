# nvim
# nvim config for arch linux
# need install
#    - "AUR" neovim-git -- for config in .LUA
#    - xclip  -- for system clipboard 
# Warning - for normal work u need:
# -- For all this stage use "nvim ." command in nvim directory !!!
# 1 - in nvim/lua/ make the plugins.lua rename for plugins.bak and delete the packer_compiled.lua - we need resync the packer
# 2 - create the empty plugins.lua in nvim/lua/ directory
# 3 - in plugins.lua insert the :

vim.cmd [[packadd packer.nvim]]

return require('packer').startup(function(use)
  use 'wbthomason/packer.nvim'
    
end)
# 4 - in opened in nvim plugins.lua make :so and :PackerSync - then ZZ (save the file and quit nvim)
# 5 - delete the "end)" from plugins lua and copy from plugins.bak all what goes after " use 'wbthomason/packer.nvim' ", dont copy " use require("rose-pine").setup() " under the vim.cmd [[packadd packer.nvim]] !!!
# 6 - in plugins.lua make the :so and :PackerSync
# 7 - After download the plugins copy " use require("rose-pine").setup() " under the vim.cmd [[packadd packer.nvim]] - :so and :PackerSync ZZ
# 8 - now go in nvim/after/plugin and :so and :PackerSync every plugin there to make sure the changes apply.
# 9 - You can learn or replase every command in nvim/lua/nickolit/remap.lua, prefencies in nvim/lua/nickolit/set.lua
# 10 - Enjoy your new vim ;-)
