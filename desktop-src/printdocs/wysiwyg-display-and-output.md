---
description: La maggior parte delle applicazioni tenta di supportare l'output in WYSIWYG (ciò che viene visualizzato è quello che si ottiene).
ms.assetid: 34a1f37c-0fbf-451b-bb55-80ad85bcd4de
title: Visualizzazione e output WYSIWYG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c03e4fa653c0d8e891cb079a7a7e7a003f9ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317273"
---
# <a name="wysiwyg-display-and-output"></a>Visualizzazione e output WYSIWYG

La maggior parte delle applicazioni tenta di supportare l'output in WYSIWYG (ciò che viene visualizzato è quello che si ottiene). Questo significa che il testo disegnato con un tipo di carattere Helvetica Bold a 10 punti nella finestra dell'applicazione dovrebbe avere un aspetto simile quando viene stampato. L'ottenimento di un vero output WYSIWYG è praticamente impossibile e anche indesiderato nella maggior parte dei casi. Ciò è dovuto, in parte, alle differenze nelle tecnologie video e stampanti; un pixel su una schermata è generalmente maggiore di un punto su una stampante laser comune. Anche le distanze di visualizzazione sono diverse; un utente del computer si trova in genere a circa due metri di cammino dallo schermo, ma gli occhi di un lettore si trovano in genere a un piè di pagina dalla pagina stampata.

Per compensare le differenze di leggibilità tra le schermate e la pagina stampata, il sistema supporta un'unità denominata pollice logico che viene sempre specificata in pixel. Per una visualizzazione video, il pollice logico è sempre maggiore del pollice fisico per compensare la distanza di visualizzazione più lunga e la risoluzione (in genere) più grossolana. Per le stampanti, il pollice logico è sempre uguale al pollice fisico.

Per ottenere un effetto WYSIWYG durante il disegno del testo, sono interessati due problemi correlati: l'aspetto di singoli caratteri è identico e il layout di pagina indipendente dal dispositivo. Per risolvere il primo problema, un'applicazione può utilizzare la funzione [**CreateFont**](/windows/desktop/api/wingdi/nf-wingdi-createfonta) per specificare il nome del tipo di carattere e le dimensioni di un tipo di carattere ideale (o logico), quindi chiamare la funzione [**SelezionaOggetto**](/windows/desktop/api/wingdi/nf-wingdi-selectobject) per identificare il contesto di visualizzazione o di stampante. Quando l'applicazione chiama **SelezionaOggetto** , il sistema seleziona un tipo di carattere fisico che rappresenta la corrispondenza più vicina possibile al tipo di carattere logico specificato. Quando il sistema seleziona il tipo di carattere visualizzato, viene scelto un tipo di carattere fisico maggiore della dimensione effettiva. Questo problema si verifica a causa del pollice logico più grande sullo schermo. Dal punto di vista dell'utente, tuttavia, sembra essere molto vicino all'altezza corretta. Quando il sistema seleziona il tipo di carattere per la stampante, viene scelto un tipo di carattere fisico che corrisponde effettivamente alla dimensione richiesta. Per altre informazioni sui tipi di carattere e l'output di testo, vedere [caratteri e testo](/windows/desktop/gdi/fonts-and-text).

Il secondo problema, quello del layout di pagina indipendente dal dispositivo, può essere risolto mediante l'uso di metriche TrueType. Questo vale anche quando si mantiene la compatibilità con le versioni di Windows a 16 bit. Per altre informazioni, vedere [uso di metriche TrueType](/windows/desktop/gdi/using-portable-truetype-metrics)portabili.

Per ottenere un effetto WYSIWYG durante il disegno di immagini bitmap, un'applicazione può recuperare la larghezza e l'altezza, in pollici logici, dello schermo e della pagina stampata. Utilizzando questi valori, l'applicazione può creare fattori di scala orizzontale e verticale per mantenere la proporzione di immagini bitmap quando vengono disegnate su una stampante. Per ulteriori informazioni sulle bitmap e sull'output bitmap, vedere [bitmap](/windows/desktop/gdi/bitmaps).

 

 
