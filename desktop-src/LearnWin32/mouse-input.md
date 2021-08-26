---
title: Input del mouse (Informazioni di base con Win32 e C++)
description: Mouse Input
ms.assetid: EB074CB6-2BB3-4593-A843-8EE25CA028BE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28ff39b798b1438bca33bc9ab9b077333dca351e32a5945b939beba2c13f5894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897046"
---
# <a name="mouse-input-get-started-with-win32-and-c"></a>Input del mouse (Informazioni di base con Win32 e C++)

Windows mouse con un massimo di cinque pulsanti: sinistro, centrale e destro, oltre a due pulsanti aggiuntivi denominati XBUTTON1 e XBUTTON2.

![figura che mostra i pulsanti sinistro (1), destro (2), centrale (3) e xbutton1 (4).](images/mouse.png)

La maggior parte dei mouse Windows avere almeno i pulsanti sinistro e destro. Il pulsante sinistro del mouse viene usato per puntare, selezionare, trascinare e così via. Il pulsante destro del mouse visualizza in genere un menu di scelta rapida. Alcuni topi hanno una rotellina di scorrimento tra i pulsanti sinistro e destro. A seconda del mouse, la rotellina di scorrimento potrebbe essere selezionabile, rendendola il pulsante centrale.

I pulsanti XBUTTON1 e XBUTTON2 si trovano spesso ai lati del mouse, vicino alla base. Questi pulsanti aggiuntivi non sono presenti in tutti i topi. Se presenti, i pulsanti XBUTTON1 e XBUTTON2 vengono spesso mappati a una funzione dell'applicazione, ad esempio lo spostamento avanti e indietro in un Web browser.

Gli utenti mancino spesso trovano più comodo scambiare le funzioni dei pulsanti sinistro e destro, usando il pulsante destro come puntatore e il pulsante sinistro per visualizzare il menu di scelta rapida. Per questo motivo, la Windows della Guida usa i termini *pulsante* primario e pulsante *secondario*, che fanno riferimento alla funzione logica anziché alla posizione fisica. Nell'impostazione predefinita (a destra) il pulsante sinistro è il pulsante primario e quello destro è il pulsante secondario. Tuttavia, i termini clic *con il pulsante destro* del mouse e clic *sinistro* fanno riferimento ad azioni logiche. *Fare clic con* il pulsante destro del mouse significa fare clic sul pulsante primario, indipendentemente dal fatto che si trova fisicamente sul lato destro o sinistro del mouse.

Indipendentemente dal modo in cui l'utente configura il mouse, Windows automaticamente i messaggi del mouse in modo che siano coerenti. L'utente può scambiare i pulsanti primario e secondario nel mezzo dell'uso del programma e non influisce sul comportamento del programma.

La documentazione MSDN usa i termini *pulsante destro* e *pulsante sinistro* per indicare il *pulsante primario* *e secondario.* Questa terminologia è coerente con i nomi dei messaggi della finestra per l'input del mouse. Tenere presente che i pulsanti fisici sinistro e destro potrebbero essere scambiati.

## <a name="next"></a>Prossima

[Risposta ai clic del mouse](mouse-clicks.md)

 

 




