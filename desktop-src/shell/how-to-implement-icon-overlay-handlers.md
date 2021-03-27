---
description: I gestori di sovrimpressione delle icone sono oggetti COM (Component Object Model in-process), implementati come dll.
ms.assetid: ADF27BFD-CC96-43F9-9EBB-DEBE0DEA7B92
title: Come implementare i gestori di sovrimpressione delle icone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22c1057f65c50b31c6627846ec77103827a0283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979535"
---
# <a name="how-to-implement-icon-overlay-handlers"></a>Come implementare i gestori di sovrimpressione delle icone

I gestori di sovrimpressione delle icone sono oggetti COM (Component Object Model in-process), implementati come dll. Esportano un'interfaccia oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellIconOverlayIdentifier**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier). Questa interfaccia ha tre metodi: [**IShellIconOverlayIdentifier:: GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo), [**IShellIconOverlayIdentifier:: GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority)e [**IShellIconOverlayIdentifier:: IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof).

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-getoverlayinfo"></a>Passaggio 1: implementazione di GetOverlayInfo

Il metodo [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) viene chiamato per la prima volta durante l'inizializzazione. Il metodo restituisce il percorso completo del file che contiene l'immagine sovrapposta all'icona e il relativo indice in base zero all'interno del file. La shell aggiunge quindi l'immagine all'elenco di immagini di sistema. Le sovrapposizioni di icone possono essere contenute in uno dei tipi di file standard, tra cui. exe,. dll e. ico.

Al termine dell'inizializzazione, la shell chiama [**GetOverlayInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getoverlayinfo) quando è necessario visualizzare la sovrapposizione dell'icona del gestore. Il metodo deve restituire lo stesso nome file e lo stesso indice che ha fatto durante l'inizializzazione. Sebbene la shell usi l'immagine memorizzata nella cache dell'elenco di immagini del sistema anziché caricare l'immagine dal file, una sovrapposizione di icone viene ancora identificata dal nome e dall'indice del file.

### <a name="step-2-implementing-getpriority"></a>Passaggio 2: implementazione di GetPriority

Il metodo [**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) viene chiamato solo durante l'inizializzazione. Assegna un valore di priorità alla sovrapposizione dell'icona del gestore. Il valore può variare da zero a 100, dove 100 è la priorità più bassa. Lo scopo di questo valore di priorità è aiutare la shell a risolvere il conflitto che si verifica quando vengono specificate più sovrapposizioni di icone per un singolo oggetto. La shell USA innanzitutto un set di regole interno per determinare la sovrapposizione dell'icona con priorità più alta. Se queste regole non consentono di risolvere il conflitto, i valori assegnati alle icone sovrapposte da **GetPriority** determinano la priorità.

Il valore di priorità impostato da [**GetPriority**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-getpriority) non è un modo affidabile per risolvere i conflitti tra i gestori sovrapposti delle icone non correlate. Non esiste alcun modo per il gestore per determinare quali valori di priorità utilizzano altri gestori. In genere, è necessario impostare il valore su zero. Tuttavia, il valore di priorità è utile quando sono stati implementati due o più gestori di sovrapposizioni di icone che possono richiedere icone di sovrapposizione icona per lo stesso oggetto. Impostando in modo appropriato i valori di priorità, è possibile specificare quale verrà visualizzata la sovrimpressione dell'icona richiesta.

### <a name="step-3-implementing-ismemberof"></a>Passaggio 3: implementazione di IsMemberOf

La shell chiama il metodo [**IsMemberOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelliconoverlayidentifier-ismemberof) per determinare se deve visualizzare la sovrimpressione dell'icona di un gestore per un oggetto specifico. La shell specifica l'oggetto passandone il nome al metodo. Se un gestore desidera che venga visualizzata la sovrimpressione dell'icona, **IsMemberOf** restituisce S \_ OK. In caso contrario, restituisce \_ false.

I gestori di sovrimpressione delle icone sono normalmente progettati per funzionare con un particolare gruppo di file. Un esempio tipico è un [tipo di file](fa-file-types.md), identificato da un'estensione di file specifica. Un gestore sovrapposizione icone può richiedere una sovrapposizione di icone per tutti i file del tipo di file. Alcuni gestori richiedono una sovrapposizione di icone solo se un file del tipo di file si trova in uno stato specifico. Tuttavia, i gestori di sovrimpressione delle icone sono liberi di richiedere la sovrapposizione delle icone per qualsiasi oggetto scelto.

 

 
