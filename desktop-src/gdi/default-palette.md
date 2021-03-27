---
description: La tavolozza predefinita è una matrice di valori di colore che identifica i colori che possono essere usati con un contesto di dispositivo per impostazione predefinita.
ms.assetid: 7972d5da-2b73-4cd7-a2ee-fca3a571f611
title: Tavolozza predefinita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c100eeb144ab4f6483281b33739578642880a91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880313"
---
# <a name="default-palette"></a>Tavolozza predefinita

La *tavolozza predefinita* è una matrice di valori di colore che identifica i colori che possono essere usati con un contesto di dispositivo per impostazione predefinita. il sistema associa la tavolozza predefinita a un contesto ogni volta che un'applicazione crea un contesto per un dispositivo che supporta le tavolozze dei colori. La tavolozza predefinita garantisce che i colori siano disponibili per l'utilizzo da parte di un'applicazione senza ulteriori azioni.

La tavolozza predefinita include in genere 20 voci (colori), ma il numero esatto di voci può variare da dispositivo a dispositivo. Questo numero è uguale al valore NUMCOLORS restituito dalla funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . Un'applicazione può recuperare i valori di colore per i colori nella tavolozza predefinita enumerando le penne solide, la stessa tecnica usata per individuare i colori disponibili sui dispositivi non tavolozza. I colori della tavolozza predefinita dipendono dal dispositivo. I dispositivi di visualizzazione, ad esempio, usano spesso i 16 colori standard dello schermo VGA e 4 altri colori definiti da Windows. I dispositivi di stampa possono utilizzare altri colori predefiniti.

Quando si usa la tavolozza predefinita, le applicazioni usano i valori dei colori per specificare i colori della penna e del testo. Se il colore richiesto non è presente nella tavolozza, il sistema si avvicina al colore utilizzando il colore più vicino nella tavolozza. Se un'applicazione richiede un colore del pennello a tinta unita non presente nella tavolozza, il sistema simula il colore in base ai colori presenti nella tavolozza.

Per evitare approssimazioni e dithering, le applicazioni possono inoltre specificare i colori di penna, pennello e testo utilizzando gli indici della tavolozza dei colori anziché i valori dei colori. Un indice della tavolozza dei colori è un valore intero che identifica una voce della tavolozza specifica. Le applicazioni possono usare gli indici della tavolozza dei colori al posto dei valori di colore, ma devono usare la macro [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) per creare gli indici.

Gli indici della tavolozza dei colori sono utili solo per i dispositivi che supportano le tavolozze dei colori. Per evitare la dipendenza da questo dispositivo, le applicazioni che utilizzano lo stesso codice per il disegno sia nei dispositivi della tavolozza che non della tavolozza devono utilizzare valori di colore relativi alla tavolozza per specificare i colori di penna, pennello e testo. Questi valori sono identici ai valori dei colori tranne quando si creano pennelli a tinta unita. (Nei dispositivi della tavolozza, un colore del pennello a tinta unita specificato da un valore di colore relativo alla tavolozza è soggetto all'approssimazione del colore anziché alla retinatura). Le applicazioni devono usare la macro [**PALETTERGB**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) per creare valori di colore relativi alla tavolozza.

Il sistema non consente a un'applicazione di modificare le voci nella tavolozza predefinita. Per usare colori diversi da quelli della tavolozza predefinita, un'applicazione deve creare una propria tavolozza logica e selezionare la tavolozza nel contesto di dispositivo.

 

 



