## Clone
    git clone -b master https://github.com/metastats/metastats.git
    cd metastats
    git checkout -b gh-pages origin/gh-pages
    git checkout -b workspace master
    git rm COPYING
    git checkout gh-pages -- index.html css data lib
    git commit -m 'My clone'
    
## Build
    cp -iv yourstats.json data/
    echo "files.push 'data/yourstats.json'" >> src/mkstats.coffee
    cake build
    git commit -am 'My build'
    
