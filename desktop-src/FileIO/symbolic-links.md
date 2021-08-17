---
description: Un collegamento simbolico è un oggetto del file system che punta a un altro file system oggetto. L'oggetto a cui punta viene chiamato destinazione.
ms.assetid: d6bf5df7-bc12-4dec-b116-95d9109f5eb4
title: Collegamenti simbolici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 126897dc230b36f504ef17653daea32b1076d10870a3a22015462f3abec05448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951030"
---
# <a name="symbolic-links"></a>Collegamenti simbolici

Un collegamento simbolico è un oggetto del file system che punta a un altro file system oggetto. L'oggetto a cui punta viene chiamato destinazione.

I collegamenti simbolici sono trasparenti per gli utenti. i collegamenti vengono visualizzati come normali file o directory e possono essere agiti dall'utente o dall'applicazione esattamente nello stesso modo.

I collegamenti simbolici sono progettati per facilitare la migrazione e la compatibilità delle applicazioni con UNIX operativi. Microsoft ha implementato i collegamenti simbolici per funzionare esattamente come UNIX collegamenti.

Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Effetti di collegamento simbolico sulle funzioni dei file system](symbolic-link-effects-on-file-systems-functions.md)<br/> | Effetto dei collegamenti simbolici sulle funzioni di file standard che usano nomi di percorso per specificare uno o più file.<br/>                                        |
| [Considerazioni sulla programmazione](symbolic-link-programming-considerations.md)<br/>                             | Considerazioni sulla programmazione per l'uso di collegamenti simbolici.<br/>                                                                                |
| [Creazione di collegamenti simbolici](creating-symbolic-links.md)<br/>                                                 | Creare collegamenti simbolici che usano un percorso assoluto o relativo usando la [**funzione CreateSymbolicLink.**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka)<br/> |



 

## <a name="supported-operating-systems"></a>Sistemi operativi supportati

I collegamenti simbolici sono disponibili in NTFS a partire da Windows Vista.

 

 




