---
title: Uso dei tavolozze
description: Uso dei tavolozze
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE messaggio
- macro capPalettePaste
- WM_CAP_PAL_OPEN messaggio
- macro capPaletteOpen
- WM_CAP_PAL_AUTOCREATE messaggio
- Macro capPaletteAuto
- WM_CAP_PAL_MANUALCREATE messaggio
- macro capPaletteManual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51f9399520b5a3cefc046959c0d59d7abe9d0f1b6ab19662f750720afd16447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686711"
---
# <a name="working-with-palettes"></a>Uso dei tavolozze

Inizialmente, se il formato di acquisizione video richiede una tavolozza, la finestra di acquisizione usa la tavolozza fornita dal driver di acquisizione. Questa tavolozza può essere costituita da valori in scala di grigi per la riproduzione in bianco e nero o da un'ampia selezione di valori di colore. È possibile recuperare un riquadro esistente per sostituire il riquadro predefinito usando il messaggio [**WM \_ CAP PAL \_ \_ PASTE**](wm-cap-pal-paste.md) o [**WM CAP PAL \_ \_ \_ OPEN**](wm-cap-pal-open.md) (o la macro [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) o [**capPaletteOpen).**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) In alternativa, è possibile creare un riquadro personalizzato per sostituire il riquadro predefinito usando il messaggio [**WM \_ CAP PAL \_ \_ AUTOCREATE**](wm-cap-pal-autocreate.md) o [**WM CAP PAL \_ \_ \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) (o la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) o [**capPaletteManual).**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) Dopo aver sostituito il riquadro predefinito, la finestra di acquisizione e il driver usano il riquadro di sostituzione fino a quando non si crea o si apre un'altra tavolozza.

Il messaggio WM \_ CAP \_ PAL \_ AUTOCREATE o WM CAP PAL MANUALCREATE crea una tavolozza \_ \_ \_ ottimizzata in base all'input video corrente. Questa tavolozza personalizzata offre a una sequenza video la migliore fedeltà dei colori perché si basa sui colori presenti nella sequenza. La finestra di acquisizione crea un istogramma tridimensionale dei colori campioni. Riduce il numero di colori esaminando l'errore assoluto tra i colori adiacenti e consolidando quelli con il valore di errore più piccolo.

Quando si invia WM CAP PAL AUTOCREATE, è necessario specificare il numero di fotogrammi da campionare per AVICap e specificare le \_ dimensioni della tavolozza dei \_ \_ colori. Quando si specifica il numero di fotogrammi, includere un numero sufficiente di fotogrammi per assicurarsi che tutti i colori nella sequenza siano campionati.

È possibile campionare il frame corrente usando WM \_ CAP \_ PAL \_ MANUALCREATE. Usando questo messaggio con diversi fotogrammi selezionati manualmente, è possibile creare una tavolozza contenente i colori da visualizzare nella tavolozza.

Una tavolozza può contenere fino a 256 colori. Se si uniscono tavolozze o se la sequenza video deve essere visualizzata contemporaneamente ad altri video o immagini, è consigliabile usare una selezione di colori più piccola in modo che i colori di ogni immagine o clip video possano coesistere.

Si salva un nuovo riquadro usando il messaggio [**WM \_ CAP PAL \_ \_ SAVE**](wm-cap-pal-save.md) (o la macro [**capPaletteSave)**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) e successivamente lo si recupera usando il messaggio [**WM CAP PAL \_ \_ \_ OPEN.**](wm-cap-pal-open.md) È possibile salvare un riquadro per la post-elaborazione della tavolozza o per l'uso in un'altra applicazione.

È possibile incollare un riquadro dagli Appunti nella finestra di acquisizione usando il messaggio [**WM \_ CAP PAL \_ \_ PASTE.**](wm-cap-pal-paste.md) La finestra di acquisizione passa la tavolozza al driver di acquisizione. Altre applicazioni possono copiare i tavolozze negli Appunti. È anche possibile copiare un riquadro negli Appunti usando il messaggio [**WM \_ CAP EDIT \_ \_ COPY**](wm-cap-edit-copy.md) (o la macro [**capEditCopy).**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) Questo messaggio copia il buffer dei fotogrammi video, inclusa la tavolozza, negli Appunti.

 

 




