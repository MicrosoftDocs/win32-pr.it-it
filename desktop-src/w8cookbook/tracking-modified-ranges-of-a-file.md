---
title: Rilevamento degli intervalli modificati di un file
description: Rilevamento degli intervalli modificati di un file
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300565"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Rilevamento degli intervalli modificati di un file

## <a name="platforms"></a>Piattaforme

**Client-** Windows 8.1 (tutti gli SKU)  
**Server-** Windows Server 2012 R2  

## <a name="description"></a>Descrizione

Il team NT file System (NTFS) ha aggiunto una nuova funzionalità di Windows. Il journal USN restituirà un record di numero di sequenza di aggiornamento (USN) contenente intervalli modificati per un file alla chiusura. È stato introdotto un nuovo tipo \_ di record, record USN \_ V4 per registrare gli intervalli modificati di un file.

La funzionalità non è abilitata per impostazione predefinita. Gli utenti devono richiamare un comando di controllo file system (FSCTL) per abilitarlo. Tuttavia, poiché altri componenti di Windows possono attivare il rilevamento dell'intervallo, gli utenti e gli sviluppatori possono percepire che la funzionalità è sempre abilitata. Windows consentirà agli sviluppatori di eseguire query sul journal USN per verificare se il rilevamento dell'intervallo è abilitato.

La documentazione MSDN verrà fornita in un secondo momento per indicare agli sviluppatori come accedere ai \_ record USN record \_ V4.

## <a name="manifestation"></a>Manifestazione

Tutte le applicazioni esistenti che utilizzano il journal USN continueranno a funzionare correttamente senza problemi di compatibilità.

 

 




