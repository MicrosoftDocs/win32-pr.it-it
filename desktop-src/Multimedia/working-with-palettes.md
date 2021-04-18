---
title: Utilizzo delle tavolozze
description: Utilizzo delle tavolozze
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- Messaggio WM_CAP_PAL_PASTE
- capPalettePaste (macro)
- Messaggio WM_CAP_PAL_OPEN
- capPaletteOpen (macro)
- Messaggio WM_CAP_PAL_AUTOCREATE
- capPaletteAuto (macro)
- Messaggio WM_CAP_PAL_MANUALCREATE
- capPaletteManual (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09cbbe3ffc8ea21d1ecf8545f036f5ba6dfb927
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297801"
---
# <a name="working-with-palettes"></a>Utilizzo delle tavolozze

Inizialmente, se il formato di acquisizione video richiede una tavolozza, la finestra di acquisizione usa la tavolozza fornita dal driver di acquisizione. Questa tavolozza può essere costituita da valori di scala in grigio per la riproduzione in bianco e nero o da un'ampia selezione di valori di colore. È possibile recuperare una tavolozza esistente per sostituire la tavolozza predefinita usando il messaggio aperto di WM Cap per la funzione [**\_ \_ \_ Incolla**](wm-cap-pal-paste.md) o [**WM \_ Cap \_ PAL \_**](wm-cap-pal-open.md) (oppure la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) o [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) ). In alternativa, è possibile creare una tavolozza personalizzata per sostituire la tavolozza predefinita usando il messaggio [**WM \_ Cap \_ PAL \_ autocreate**](wm-cap-pal-autocreate.md) o [**WM \_ Cap \_ PAL \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (o la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) o [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) ). Dopo aver sostituito la tavolozza predefinita, la finestra di acquisizione e il driver utilizzano la tavolozza di sostituzione fino a quando non si crea o si apre un'altra tavolozza.

Il \_ messaggio WM Cap \_ PAL \_ autocreate o WM \_ Cap \_ PAL \_ MANUALCREATE crea una tavolozza ottimizzata in base all'input video corrente. Questa tavolozza personalizzata offre una sequenza video la massima fedeltà del colore perché si basa su colori presenti nella sequenza. La finestra di acquisizione crea un istogramma tridimensionale dei colori campionati. Riduce il numero di colori esaminando l'errore assoluto tra i colori adiacenti e consolidando quelli con il valore di errore più basso.

Quando si invia \_ la \_ \_ creazione autocreata di WM Cap, è necessario specificare il numero di frame per l'esempio di AVICap e specificare le dimensioni della tavolozza dei colori. Quando si specifica il numero di frame, includere un numero sufficiente di fotogrammi per assicurarsi che tutti i colori nella sequenza siano campionati.

È possibile campionare il frame corrente usando WM \_ Cap \_ PAL \_ MANUALCREATE. Utilizzando questo messaggio con diversi frame selezionati manualmente, è possibile creare una tavolozza contenente i colori che si desidera visualizzare nella tavolozza.

Una tavolozza può contenere fino a 256 colori. Se si uniscono le tavolozze o se la sequenza video deve essere visualizzata simultaneamente con altre immagini o video, è consigliabile usare una selezione di colori più piccola in modo che i colori di ogni clip immagine o video possano coesistere.

È possibile salvare una nuova tavolozza usando il messaggio di [**\_ \_ \_ salvataggio di WM Cap**](wm-cap-pal-save.md) , o la macro [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) , e successivamente recuperarla usando il messaggio di [**apertura di WM \_ Cap \_ PAL \_**](wm-cap-pal-open.md) . È possibile salvare una tavolozza per la post-elaborazione della tavolozza o per l'uso in un'altra applicazione.

È possibile incollare una tavolozza dagli Appunti nella finestra di acquisizione usando il messaggio [**di \_ \_ \_ incollamento PAL di WM Cap**](wm-cap-pal-paste.md) . La finestra di acquisizione passa la tavolozza al driver di acquisizione. Altre applicazioni possono copiare le tavolozze negli Appunti. È anche possibile copiare una tavolozza negli appunti usando il messaggio [**di \_ \_ \_ copia di modifica di WM Cap**](wm-cap-edit-copy.md) (o la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). Questo messaggio copia il buffer del frame video, inclusa la tavolozza, sugli Appunti.

 

 




