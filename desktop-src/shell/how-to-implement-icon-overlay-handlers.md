---
description: I gestori di sovrimpressione delle icone sono oggetti Component Object Model (COM) in-process, implementati come DLL.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Come implementare gestori di sovrimpressione delle icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8745d0d5c0cf9c69f28f0235ecc82acb07a14f1e3408d7fa7d65cf729e01403f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859698"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Come implementare gestori di sovrimpressione delle icone

I gestori di sovrimpressione delle icone sono oggetti Component Object Model (COM) in-process, implementati come DLL. Esportano un'interfaccia oltre a [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Questa interfaccia ha tre metodi: [**IShellIconOverlayIdentifier::GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**IShellIconOverlayIdentifier::GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)e [**IShellIconOverlayIdentifier::IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-getoverlayinfo"></a>Passaggio 1: Implementazione di GetOverlayInfo

Il [**metodo GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) viene chiamato prima durante l'inizializzazione. Il metodo restituisce il percorso completo del file che contiene l'immagine di sovrimpressione dell'icona e il relativo indice in base zero all'interno del file. La shell aggiunge quindi l'immagine all'elenco di immagini di sistema. Le sovrimpressione delle icone possono essere contenute in uno qualsiasi dei tipi di file standard, inclusi .exe, .dll e ico.

Al termine dell'inizializzazione, la shell chiama [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) quando deve visualizzare la sovrimpressione dell'icona del gestore. Il metodo deve restituire lo stesso nome file e lo stesso indice che ha restituito durante l'inizializzazione. Anche se la shell usa l'immagine memorizzata nella cache nell'elenco di immagini di sistema anziché caricare l'immagine dal file, una sovrimpressione dell'icona viene comunque identificata dal nome file e dall'indice.

### <a name="step-2-implementing-getpriority"></a>Passaggio 2: Implementazione di GetPriority

Il [**metodo GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) viene chiamato solo durante l'inizializzazione. Assegna un valore di priorità alla sovrimpressione dell'icona del gestore. Il valore può variare da zero a 100, dove 100 è la priorità più bassa. Lo scopo di questo valore di priorità è aiutare la shell a risolvere il conflitto che si verifica quando vengono specificate più sovrimpressione di icone per un singolo oggetto. La shell usa innanzitutto un set interno di regole per determinare la sovrimpressione dell'icona con priorità più alta. Se queste regole non risolvono il conflitto, i valori assegnati alle sovrimpressione dell'icona da **GetPriority** determinano la priorità.

Il valore di priorità impostato [**da GetPriority non**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) è un modo affidabile per risolvere i conflitti tra gestori di sovrimpressione delle icone non correlate. Non è possibile per il gestore determinare quali valori di priorità vengono utilizzati da altri gestori. In genere, è necessario impostare il valore su zero. Tuttavia, il valore di priorità è utile quando sono stati implementati due o più gestori di sovrimpressione delle icone che possono richiedere icone di sovrimpressione icona per lo stesso oggetto. Impostando i valori di priorità in modo appropriato, è possibile specificare quali sovrimpressione delle icone richieste verranno visualizzate.

### <a name="step-3-implementing-ismemberof"></a>Passaggio 3: Implementazione di IsMemberOf

La shell chiama il [**metodo IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) per determinare se deve visualizzare la sovrimpressione dell'icona di un gestore per un determinato oggetto. La shell specifica l'oggetto passandone il nome al metodo . Se un gestore vuole visualizzare la sovrimpressione dell'icona, **IsMemberOf** restituisce S \_ OK. In caso contrario, restituisce S \_ FALSE.

I gestori di sovrimpressione delle icone sono in genere destinati a funzionare con un particolare gruppo di file. Un esempio tipico è un [tipo di file](fa-file-types.md), identificato da un'estensione di file specifica. Un gestore di sovrimpressione dell'icona può richiedere una sovrimpressione dell'icona per tutti i file del tipo di file. Alcuni gestori richiedono una sovrimpressione dell'icona solo se un file del tipo di file si trova in uno stato specifico. Tuttavia, i gestori di sovrimpressione delle icone possono richiedere la sovrimpressione dell'icona per qualsiasi oggetto scelto.

 

 
