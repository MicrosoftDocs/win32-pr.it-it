---
title: Esempi di animazioni Windows
description: Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione di Windows Animation Manager.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animazione Windows Animation Windows, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331644"
---
# <a name="windows-animation-samples"></a>Esempi di animazioni Windows

Negli argomenti contenuti in questa sezione vengono fornite informazioni dettagliate sugli esempi di codice che supportano la documentazione di Windows Animation Manager.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                     | Descrizione                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Esempio di animazione basata su applicazioni](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Esempio di animazione basata su timer](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Esempio di interpolazione personalizzata](custom-interpolator-sample.md)<br/>                   | Viene illustrato come utilizzare l'animazione Windows con un interpolatore personalizzato, con Direct2D utilizzato per il rendering. <br/> |
| [Esempio di layout di griglia](grid-layout-sample.md)<br/>                                   | Viene illustrato come utilizzare l'animazione Windows utilizzando Direct2D per animare una griglia di immagini. <br/>                         |
| [Esempio di confronto prioritario](priority-comparison-sample.md)<br/>                   | Viene illustrato come utilizzare l'animazione Windows con un confronto prioritario tramite Direct2D per il rendering.<br/>      |



 

## <a name="sample-files"></a>File di esempio

Ogni esempio contiene molti dei file di chiave seguenti:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp
</dt> <dd>

Definisce il punto di ingresso dell'applicazione.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h
</dt> <dd>

Dichiara la classe CMainWindow.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp
</dt> <dd>

Inizializza i componenti di animazione e la piattaforma grafica, carica le immagini ed esegue il rendering dell'area client.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h
</dt> <dd>

Dichiara la classe CLayoutManager.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp
</dt> <dd>

Calcola il layout delle immagini nella finestra principale, crea gli storyboard, aggiunge le transizioni allo storyboard e pianifica lo storyboard.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Anteprima. h
</dt> <dd>

Dichiara la classe CThumbNail.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Anteprima. cpp
</dt> <dd>

Crea variabili di animazione ed esegue il rendering delle anteprime.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida allo sviluppo di animazioni Windows](windows-animation-developer-guide.md)
</dt> <dt>

[Informazioni di riferimento sull'animazione Windows](windows-animation-reference.md)
</dt> </dl>

 

 





