---
title: Windows Esempi di animazione
description: Gli argomenti contenuti in questa sezione forniscono informazioni dettagliate sugli esempi di codice che supportano la documentazione Windows Animation Manager.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Windows Animation Windows Animation ,samples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9119ab7333f1f5d74b9be9998ad26b36139f9a92d88fec856d3f4572d12f431
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656151"
---
# <a name="windows-animation-samples"></a>Windows Esempi di animazione

Gli argomenti contenuti in questa sezione forniscono informazioni dettagliate sugli esempi di codice che supportano la documentazione Windows Animation Manager.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Esempio di animazione basata su applicazioni](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Esempio di animazione basata su timer](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Esempio di interpolatore personalizzato](custom-interpolator-sample.md)<br/>                   | Illustra come usare l'Windows con un interpolatore personalizzato, con Direct2D usato per il rendering. <br/> |
| [Esempio di layout griglia](grid-layout-sample.md)<br/>                                   | Illustra come usare l'Windows, usando Direct2D per animare una griglia di immagini. <br/>                         |
| [Esempio di confronto delle priorità](priority-comparison-sample.md)<br/>                   | Illustra come usare l'Windows con un confronto di priorità personalizzato, usando Direct2D per il rendering.<br/>      |



 

## <a name="sample-files"></a>File di esempio

Ogni esempio contiene molti dei file chiave seguenti:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp
</dt> <dd>

Definisce il punto di ingresso dell'applicazione.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h
</dt> <dd>

Dichiara la classe CMainWindow.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp
</dt> <dd>

Inizializza i componenti dell'animazione e la piattaforma grafica, carica le immagini ed esegue il rendering dell'area client.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h
</dt> <dd>

Dichiara la classe CLayoutManager.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp
</dt> <dd>

Calcola il layout delle immagini nella finestra principale, crea storyboard, aggiunge transizioni allo storyboard e pianifica lo storyboard.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h
</dt> <dd>

Dichiara la classe CThumbNail.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp
</dt> <dd>

Crea variabili di animazione ed esegue il rendering delle anteprime.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Guida allo sviluppo di animazioni](windows-animation-developer-guide.md)
</dt> <dt>

[Windows Informazioni di riferimento sulle animazioni](windows-animation-reference.md)
</dt> </dl>

 

 





