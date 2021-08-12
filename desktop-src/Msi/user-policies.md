---
description: Criteri di sistema utente usati con il Windows installer.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Criteri utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ce52f4a691729c71ed57ddba8dd80811681844e1ba6c02664ee50c11f8d0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623090"
---
# <a name="user-policies"></a>Criteri utente

I criteri utente seguenti possono essere configurati in

**HKEY \_ Current \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**



| Nome del valore                                                            | Tipi di dati value          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Se questo valore è impostato su "1" e viene impostato anche il valore del computer corrispondente, il programma di installazione viene sempre installato con privilegi elevati.<br/> In caso contrario, il programma di installazione usa privilegi elevati per installare applicazioni gestite e usa il livello di privilegio dell'utente corrente per le applicazioni non gestite.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Se il criterio [DisableMedia](disablemedia.md) è impostato su "1", a utenti e amministratori che eseguono un'installazione di manutenzione di un prodotto non è consentito usare la finestra di dialogo Sfoglia per esplorare le origini dei supporti, ad esempio CD-ROM, per le origini di altri prodotti installabili. La ricerca di altri prodotti non viene consentita indipendentemente dal fatto che l'installazione sia con privilegi elevati. È comunque possibile che l'utente reinstalli il prodotto dai supporti se l'utente ha un'origine multimediale etichettata correttamente.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Se questo valore è impostato su "1", il programma di installazione non archivierà i file di rollback durante l'installazione, disabilitando il rollback dell'installazione. Per impostazione predefinita, il rollback è abilitato. È consigliabile che gli amministratori non usino questo criterio a meno che non sia assolutamente essenziale.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **REG \_ SZ**<br/>    | Ordine in cui il programma di installazione cerca i tre diversi tipi di origini:<br/> "n": rete<br/> "m": supporto (CD-ROM o DVD)<br/> "u": URL (Uniform Resource Locator)<br/> Ad esempio, il valore "nmu" indica al programma di installazione di cercare prima le origini di rete, le origini multimediali seconde le origini URL per ultime. L'ostrazione di una lettera rimuove il tipo di volume corrispondente dalla ricerca. L'ordine predefinito in assenza di questo valore è network first, quindi media seguito da URL.<br/>          |
| [Criteri TransformsAtSource](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | Se questo valore esiste ed è impostato su "1"; il programma di installazione cerca i file di trasformazione nella radice di qualsiasi origine di rete [**nell'elenco di origine**](sourcelist.md) per il prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Dati applicazioni del profilo di un utente.<br/>                                                                                                                                                                                                                                             |



 

 

 




