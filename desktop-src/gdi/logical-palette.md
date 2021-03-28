---
description: Una tavolozza logica è una tavolozza dei colori che un'applicazione crea e associa a un determinato contesto di dispositivo.
ms.assetid: 7cc86771-237d-4539-8f48-2474edb764a4
title: Tavolozza logica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597e049c4320ff3ac30099e767c35a3438237904
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978567"
---
# <a name="logical-palette"></a>Tavolozza logica

Una *tavolozza logica* è una tavolozza dei colori che un'applicazione crea e associa a un determinato contesto di dispositivo. Le tavolozze logiche consentono alle applicazioni di definire e usare i colori che soddisfano le proprie esigenze specifiche. Le applicazioni possono creare un numero qualsiasi di tavolozze logiche, usandole per contesti di dispositivo separati o passando tra di essi per un singolo contesto di dispositivo. Il numero massimo di tavolozze che un'applicazione può creare dipende dalle risorse del sistema.

Un'applicazione crea una tavolozza logica tramite la funzione [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) . L'applicazione compila una struttura [**LOGPALETTE**](/windows/win32/api/wingdi/ns-wingdi-logpalette) , che specifica il numero di voci e i valori di colore per ogni voce, quindi l'applicazione passa la struttura a **CreatePalette**. La funzione restituisce un handle della tavolozza utilizzato dall'applicazione in tutte le operazioni successive per identificare la tavolozza. Per utilizzare i colori nella tavolozza logica, l'applicazione seleziona la tavolozza in un contesto di dispositivo utilizzando la funzione [**SelectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-selectpalette) e quindi realizza la tavolozza utilizzando la funzione [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) . I colori della tavolozza sono disponibili non appena viene realizzata la tavolozza logica.

Un'applicazione deve limitare le dimensioni delle tavolozze logiche a un numero sufficiente di voci per rappresentare i colori necessari. Le applicazioni non possono creare tavolozze logiche superiori alla dimensione massima della tavolozza, un valore dipendente dal dispositivo. Le applicazioni possono ottenere le dimensioni massime usando la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) per recuperare il valore SIZEPALETTE.

Sebbene un'applicazione possa specificare qualsiasi valore di colore per una determinata voce in una tavolozza logica, non tutti i colori possono essere generati dal dispositivo specificato. Il sistema non fornisce un modo per individuare i colori supportati, ma l'applicazione può individuare il numero totale di questi colori recuperando la risoluzione dei colori del dispositivo. La risoluzione dei colori, specificata nei bit di colore per pixel, è uguale al valore COLORRES restituito dalla funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . Un dispositivo con risoluzione dei colori pari a 18 ha 262.144 colori possibili. Se un'applicazione richiede un colore non supportato, il sistema sceglie un'approssimazione appropriata.

Una volta creata una tavolozza logica, un'applicazione può modificare i colori della tavolozza utilizzando la funzione [**SetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-setpaletteentries) . Se la tavolozza logica è stata selezionata e realizzata, la modifica della tavolozza non influisce immediatamente sui colori visualizzati. Per aggiornare i colori, l'applicazione deve utilizzare le funzioni [**UnrealizeObject**](/windows/desktop/api/Wingdi/nf-wingdi-unrealizeobject) e [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) . In alcuni casi, è possibile che l'applicazione debba deselezionare, deselezionare, selezionare e realizzare la tavolozza logica per assicurarsi che i colori vengano aggiornati esattamente come richiesto. Se un'applicazione seleziona una tavolozza logica in più di un contesto di dispositivo, le modifiche apportate alla tavolozza logica hanno effetto su tutti i contesti di dispositivo per i quali è selezionata.

Un'applicazione può modificare il numero di voci in una tavolozza logica tramite la funzione [**ResizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-resizepalette) . Se l'applicazione riduce le dimensioni, le voci rimanenti restano invariate. Se l'applicazione estende le dimensioni, il sistema imposta il colore per ogni nuova voce su nero (0, 0, 0) e il flag su zero.

Un'applicazione può recuperare i valori relativi al colore e al flag per le voci in una tavolozza logica specificata tramite la funzione [**GetPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getpaletteentries) . Un'applicazione può recuperare l'indice per la voce in una tavolozza logica specificata che corrisponde maggiormente a un valore di colore specificato tramite la funzione [**GetNearestPaletteIndex**](/windows/desktop/api/Wingdi/nf-wingdi-getnearestpaletteindex) .

Quando un'applicazione non necessita più di una tavolozza logica, può eliminarla usando la funzione [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) . Prima di eliminare la tavolozza, l'applicazione deve assicurarsi che la tavolozza logica non sia più selezionata in un contesto di dispositivo.

 

 



