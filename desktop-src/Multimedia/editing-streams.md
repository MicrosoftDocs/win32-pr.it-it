---
title: Modifica di flussi
description: Modifica di flussi
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream (funzione)
- EditStreamCut (funzione)
- EditStreamCopy (funzione)
- EditStreamPaste (funzione)
- EditStreamClone (funzione)
- EditStreamSetInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471462"
---
# <a name="editing-streams"></a>Modifica di flussi

È possibile creare un flusso che è possibile modificare usando la funzione [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) . Questa funzione Inizializza l'ambiente per la modifica di un flusso. Ciò include la creazione di un'interfaccia per il nuovo flusso e le tabelle di modifica interne che rilevano le modifiche apportate al flusso. **CreateEditableStream** restituisce un puntatore di flusso a un flusso modificabile richiesto da altre funzioni di modifica del flusso. Il puntatore di flusso modificabile può essere usato anche da altre funzioni AVIFile che accettano i puntatori di flusso.

È possibile tagliare uno o più esempi da un flusso modificabile usando la funzione [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) . Per rimuovere gli esempi dal flusso modificabile, questa funzione aggiunge una voce alla tabella di modifica. La funzione quindi inserisce una copia degli esempi tagliati in un nuovo flusso temporaneo il cui puntatore di interfaccia viene restituito in una variabile.

È possibile copiare uno o più esempi da un flusso modificabile in un flusso temporaneo usando la funzione [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) . **EditStreamCopy** inserisce copie degli esempi in un nuovo flusso temporaneo il cui puntatore di interfaccia viene restituito in una variabile.

È possibile copiare uno o più esempi da un flusso e incollarli in un flusso modificabile usando la funzione [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) . Per inserire gli esempi in corrispondenza della posizione specificata, questa funzione aggiunge una voce nella tabella di modifica del flusso modificabile di destinazione.

È possibile duplicare un flusso modificabile usando la funzione [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) . Questa funzione restituisce un puntatore all'interfaccia del flusso del nuovo flusso. È possibile copiare questi flussi negli Appunti o usarli per mantenere una traccia delle modifiche apportate a un flusso.

È possibile modificare molte delle caratteristiche di un flusso modificabile usando la funzione [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) . Questa funzione aggiorna l'impostazione di priorità, la lingua, la scala e la velocità, l'ora di inizio, l'impostazione della qualità, le dimensioni e le coordinate del rettangolo di destinazione e la descrizione testuale del flusso. Questi elementi vengono archiviati nella struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) associata al flusso modificabile.

È anche possibile modificare la descrizione testuale di un flusso modificabile usando la funzione [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) . Questa funzione aggiorna il membro **szName** della struttura **AVISTREAMINFO** associata al flusso modificabile.

Le funzioni di modifica funzionano sui flussi. È necessario tagliare e incollare ogni flusso singolarmente, quindi utilizzare la funzione [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) per creare un nuovo puntatore di file.

> [!Note]  
> Le tabelle di modifica in un flusso modificabile mantengono tutte le modifiche per un flusso. Il flusso di origine non viene mai modificato.

 

 

 




