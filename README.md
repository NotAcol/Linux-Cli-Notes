# Usefull CLI Tools

Γενικά ότι γράφω εδώ μπες στο συνήθειο να το κάνεις man ή καλύτερα tldr. 

Και ακόμα ποιο σημαντικό με tab κάνει auto complete στο τερματικό άλλα στα πιο πολλά shell είναι άθλιο από μονό του οπότε googlare κάνα plugin να το κάνεις καλύτερο θα σε σώσει!

## Essentials

#### [bash](https://www.youtube.com/watch?v=IYZDIhfAUM0) και τα [scripts](https://www.youtube.com/watch?v=4ygaA_y1wvQ) της. 
> [!NOTE]
>Ακόμα και αν δεν χρησιμοποιείς bash ως το shell σου οπός εγώ θα θέλεις μάλλον σίγα σίγα να την μάθεις για τα scripts της που δουλεύουν σε όλα τα συστήματα Unix (Mac & linux). Επίσης τα βασικά είναι σε όλα τα posix shells ίδια.

| Βασική | Καλύτερη |
| :---: | :---: |
| man | [tldr](https://github.com/tealdeer-rs/tealdeer) |
| cd  | [zoxide](https://github.com/ajeetdsouza/zoxide) |
| ls  | [eza](https://github.com/eza-community/eza) |
| find | [fd](https://github.com/sharkdp/fd) |
| grep | [rg](https://github.com/BurntSushi/ripgrep) |
| diff | [delta](https://github.com/dandavison/delta) |

#### ssh/scp

#### curl

#### less
> [!TIP]
> Κανε pipe την έξοδο άλλων πραγμάτων με το σύμβολο | στο less (-R flag άμα κάνεις output χρώματα) για να την διαβάσεις.


## Good to haves

#### [Yazi](https://github.com/sxyazi/yazi)
> [!IMPORTANT]
> God's gift to file browsing.

#### [fzf](https://github.com/junegunn/fzf)
> [!TIP]
> Fuzzy finder.

#### [bat](https://github.com/sharkdp/bat)
> [!TIP]
> Better cat.

#### [tmux](https://github.com/tmux/tmux/wiki)
> [!TIP] 
> Terminal multiplexer(tabs κλπ). Είναι λίγο aids να κάνεις το setup του μονός σου.

#### [trash](https://github.com/andreafrancia/trash-cli)
> [!TIP] 
> Trashcan αντί για να διαγράφεις πάντα μόνιμα με το rm.

#### [btop](https://github.com/aristocratos/btop) και [btm](https://github.com/ClementTsang/bottom)
> [!TIP] 
> TUI resource monitor σαν το alt+shift+esc των windows. btop είναι καλύτερο imo.

#### [atuin](https://github.com/atuinsh/atuin)
> [!TIP]
> Better command history.

#### [gdu](https://github.com/dundee/gdu)
> [!TIP]
> Δείχνει το μέγεθος των αρχείων με interactive τρόπο για να μπορείς να καθαρίσεις τον δίσκο.

#### [Pass](https://www.youtube.com/watch?v=FhwsfH2TpFA)
> [!TIP]
> Password manager από το τερματικό με git support. Μπορείς να ανεβάσεις τα password sto github!

#### [lazygit](https://github.com/jesseduffield/lazygit)
> [!TIP]
> TUI (Terminal User Interface) για το git. Τέρμα πιο κάλο από να κάνεις rawdog το git.


#### [thefuck](https://github.com/nvbn/thefuck)
> [!TIP]
> Άμα κάνεις ορθογραφικό σε ένα command η ξεχάσεις το sudo μπορείς να γράψεις fuck σαν επομένη εντολή και το thefuck θα προσπαθήσει να διορθώσει ότι λάθος έκανες.

#### [stow](https://www.youtube.com/watch?v=y6XCebnB9gs)
> [!TIP]
> Βοηθάει πολύ με τα dotfiles (settings) για το linux. Για περισσότερα δες το link.


# Βασικές εντολές
- Ctrl+Shift+c κάνει copy Ctrl+Shift+v κάνει paste.

- Ctrl+l για να κάνεις clear γρήγορα. Ctrl+c για να κλείσουμε ένα πρόγραμμα (αντίστοιχο του X στα προγράμματα με γραφικό περιβάλλον). Ctrl+z για να βάλουμε ένα πρόγραμμα στο background το οποίο μπορούμε να επαναφέρουμε στο foreground με `❯ fg`. 

- Μπορούμε να ανοίξουμε ένα πρόγραμμα κατευθείαν στο background προσθέτοντας το σύμβολο & στο τέλος μιας εντολής πχ `❯ vim ./file.txt &` θα ανοίξει το vim με το αρχείο file.txt άλλα δεν θα δούμε κάτι μέχρι να γράψουμε fg. 

- Μπορούμε να έχουμε πολλά προγράμματα να τρέχουν στο background και για να φέρουμε ένα συγκεκριμένο στο foreground κάνουμε `❯ fg id_number`.

- Μπορούμε να κάνουμε πολλές εντολές την μια μετά την άλλη με τους χαρακτήρες && πχ `❯ touch ./new_file && nvim ./newfile` θα δημιουργήσει ένα αρχείο new_file και μετά θα το ανοίξει με το neovim.

- Το σύμβολο . όταν μιλάμε για directory σημαίνει το pwd (directory που βρισκόμαστε τώρα) οπότε μπορείς να το χρησιμοποιήσεις για relative path πχ `❯ cd ./blah`  σε πάει στο directory blah που είναι κάτω από το pwd. Το σύμβολο .. είναι το από πάνω directory και άρα `❯ cd ../blah` σε πάει ένα directory πίσω και μετά στο directory blah.

- Το σύμβολο . στην αρχή ενός αρχείου ή directory το κάνει κρυφό πχ .secret_file

- Το σύμβολο ~ είναι συντομογραφία για το home directory του τωρινού user, οπότε `❯ cd ~/.config/` θα σε πάει στο /home/username/.config 

- Το `cd -` θα σε πάει στο προηγούμενο directory. Μπορείς να κάνεις το ίδιο πράγμα με περισσότερα από ένα directories με τις εντολές pushd popd που λειτουργούν ως stack. 
```bash
❯ cd dotfiles
❯ pwd
/home/acol/dotfiles
❯ pushd
~ ~/dotfiles
❯ cd micro
❯ pwd
/home/acol/Documents/micro
❯ popd
~/dotfiles
```

- `❯ cp target destination` για copy. `❯ rm target` για delete(remove) `❯ mv target destination` για move, μπορείς να βάλεις το target της mv στο ίδιο directory ουσιαστικά κάνοντας rename το αρχείο.

- Όταν θέλεις να κάνεις copy, delete κλπ ένα directory πρέπει να βάλεις το flag -r για να το κάνεις recursively (να κάνει delete ή copy και ότι φάκελο η αρχείο είναι από κάτω).

- Μπορείς να χρησιμοποιήσεις τον χαρακτήρα | για να κάνεις pipe το stdout ενός προγράμματος στο stdin ενός άλλου. Πολύ χρήσιμο για το less και fzf. Μπορείς επίσης να αναδιοχετεύσεις το stderr στο stdout ώστε να το κάνεις pipe κάπου πχ `❯ command1 2>&1 | command2`

- Μπορείς να διοχετεύσεις το stdout ενός προγράμματος σε ένα αρχείο με το >. Αν δεν θες να διαγράψεις τα δεδομένα που βρίσκονται είδη στο αρχείο άλλα άπλα θες να προσθέσεις ότι νέο στο τέλος του (concatenate) χρησιμοποίησε τους χαρακτήρες >>. Πχ `❯ cat some_file >> other_file`. 

- Η εντολή `❯ head --lines 10 ./file` κάνει cat τις 10 πρώτες γραμμές του αρχείου file ενώ η εντολή tail κάνει το ίδιο για τις τελευταίες. Η εντολή tail είναι πολύ χρήσιμη για να βλέπουμε logs με το flag --follow που συνεχίζει να κάνει cat μέχρι να δώσουμε Ctrl-C.

## Tips & Tricks

1. Μπορείς να βάλεις το `export MANPAGER='nvim +Man!'` στο .bashrc ή .zshrc ανάλογα το shell σου για να χρησιμοποιείς το neovim για pager της εντολής man αντί για το less.

2. Βάλε `alias manpages='man -k . | fzf | awk '\''{print $1$2}'\'' | xargs man'` στο .bashrc ή .zshrc ανάλογα το shell σου για να ορίσεις το command `manpages` που ανοίγει ένα παράθυρο fzf με όλα τα man pages που έχεις στο pc και όποιο επιλέξεις το ανοίγει.

3. Άμα κάνεις `❯ !!` στο τερματικό θα επαναλάβει την προηγουμένη εντολή. Μπορείς να κάνεις `❯ sudo !!` για να την κάνεις ως super user.

4. Με την eza μπορείς να δόσεις flag -T για tree view και με το -L *number* μπορείς να του πεις μέχρι τι βάθος να δείξει τους φακέλους. Με το flag -h προσθέτει τίτλους στην πρώτη γραμμή. Τα άλλα options όπως -al είναι σαν την ls.

5. Αν χρησιμοποιείς το ssh συχνά δες το [documenation](https://wiki.archlinux.org/title/OpenSSH) του arch wiki για config και κλειδιά και επίσης μάλλον δες [sshs](https://github.com/quantumsheep/sshs)

6. Η bat έχει themes.

7. Με την fzf το flag -e θα σου ψάξει το string που του γράφεις ενωμένο και όχι οπός θέλει. Άμα την χρησιμοποιήσεις χωρίς το flag για να ψάξεις κάτι θα δεις τι εννοώ.
