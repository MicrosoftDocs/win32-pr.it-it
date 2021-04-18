---
description: Un collegamento simbolico è un oggetto di file System che punta a un altro oggetto file system. L'oggetto a cui si fa riferimento è denominato destinazione.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f051beb7de0280ba42df782264cef385f8d01a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316766"
---
# <a name="symbolic-links"></a>Collegamenti simbolici

Un collegamento simbolico è un oggetto di file System che punta a un altro oggetto file system. L'oggetto a cui si fa riferimento è denominato destinazione.

I collegamenti simbolici sono trasparenti per gli utenti. i collegamenti vengono visualizzati come normali file o directory e possono essere utilizzati dall'utente o dall'applicazione esattamente allo stesso modo.

I collegamenti simbolici sono progettati per facilitare la migrazione e la compatibilità delle applicazioni con i sistemi operativi UNIX. Microsoft ha implementato i collegamenti simbolici per funzionare esattamente come i collegamenti UNIX.

Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Effetti dei collegamenti simbolici sulle funzioni di file System](symbolic-link-effects-on-file-systems-functions.md)<br/> | Il modo in cui i collegamenti simbolici influiscono sulle funzioni file standard che usano nomi di percorso per specificare uno o più file.<br/>                                        |
| [Considerazioni sulla programmazione](symbolic-link-programming-considerations.md)<br/>                             | Considerazioni sulla programmazione per l'utilizzo di collegamenti simbolici.<br/>                                                                                |
| [Creazione di collegamenti simbolici](creating-symbolic-links.md)<br/>                                                 | Creare collegamenti simbolici che usano un percorso assoluto o relativo tramite la funzione [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) .<br/> |



 

## <a name="supported-operating-systems"></a>Sistemi operativi supportati

I collegamenti simbolici sono disponibili in NTFS a partire da Windows Vista.

 

 




