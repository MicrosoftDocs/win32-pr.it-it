---
title: Rilevamento degli intervalli modificati di un file
description: Rilevamento degli intervalli modificati di un file
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6998d2706cd4d8bdb4e94b95fd0e617dbbf4e3a1b288d33dbcebe5528d544c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852028"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Rilevamento degli intervalli modificati di un file

## <a name="platforms"></a>Piattaforme

**Client -** Windows 8.1 (tutti gli SKU)  
**Server -** Windows Server 2012 R2  

## <a name="description"></a>Descrizione

Il team di NT File System (NTFS) ha aggiunto una nuova funzionalità per Windows. Il journal USN restituisce un record del numero di sequenza di aggiornamento (USN) contenente gli intervalli modificati per un file alla chiusura. È stato introdotto un nuovo tipo di record, USN \_ RECORD \_ V4, per registrare questi intervalli modificati di un file.

La funzionalità non è abilitata per impostazione predefinita. gli utenti devono richiamare un file system di controllo di accesso (FSCTL) per abilitarlo. Tuttavia, poiché altri componenti Windows possono attivare il rilevamento degli intervalli, gli utenti e gli sviluppatori potrebbero aver percepito che la funzionalità è sempre abilitata. Windows consentirà agli sviluppatori di eseguire query sul journal USN per verificare se il rilevamento degli intervalli è abilitato.

La documentazione MSDN verrà fornita in un secondo momento per indicare agli sviluppatori come accedere ai record USN \_ RECORD \_ V4.

## <a name="manifestation"></a>Manifestazione

Tutte le applicazioni esistenti che usano USN Journal continueranno a funzionare correttamente senza problemi di compatibilità.

 

 




