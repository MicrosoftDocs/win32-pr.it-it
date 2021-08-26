---
title: Compilatore del catalogo per i negozi online di tipo 1
description: Compilatore del catalogo per i negozi online di tipo 1
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player negozi online, compilatore di cataloghi
- negozi online, compilatore di catalogo
- tipo 1 negozi online, compilatore di catalogo
- Windows Media Player negozi online, catcomp.exe
- negozi online, catcomp.exe
- Tipo 1 di negozi online, catcomp.exe
- compilatore catalog
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2764da5e19c84145bd0a11127aebc8f518031744626ca1b41c75c43c6e10093f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864211"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a>Compilatore del catalogo per i negozi online di tipo 1

Il compilatore del catalogo (catcomp.exe) è uno strumento da riga di comando usato dai negozi online di tipo 1 per compilare il set di file TSV (Tab-Separated-Value) contenenti i dati del catalogo del negozio online in un catalogo compresso che può essere scaricato da Windows Media Player. Il compilatore del catalogo compila anche i file di aggiornamento del catalogo contenenti solo le informazioni del catalogo modificate dopo l'ultimo aggiornamento del catalogo.

I file di catalogo compressi o i file di aggiornamento del catalogo devono essere forniti Windows Media Player per il download nell'implementazione del plug-in del negozio online [di IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).

Attività comuni

-   [Compilazione di un catalogo completo da file TSV](compiling-a-full-catalog-from-tsv-files.md)
-   [Compilazione di un aggiornamento del catalogo da cataloghi completi](compiling-a-catalog-update-from-full-catalogs.md)

Attività di diagnostica

-   [Visualizzazione della Guida](displaying-help.md)
-   [Recupero delle informazioni del catalogo](retrieving-catalog-information.md)
-   [Applicazione di un aggiornamento a un catalogo](applying-an-update-to-a-catalog.md)

 

 




