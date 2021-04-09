---
description: Criteri di sistema utente utilizzati con la Windows Installer.
ms.assetid: 74e940a1-dc7c-4ea3-ab62-d118204dac3e
title: Criteri utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cec4066e4d8267b2750d538e691d91382550fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878678"
---
# <a name="user-policies"></a>Criteri utente

I criteri utente seguenti possono essere configurati in

**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**



| Nome del valore                                                            | Tipi di dati value          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlwaysInstallElevated](alwaysinstallelevated.md)<br/>         | **REG \_ DWORD**<br/> | Se questo valore è impostato su "1" e viene impostato anche il valore del computer corrispondente, il programma di installazione viene sempre installato con privilegi elevati.<br/> In caso contrario, il programma di installazione utilizza privilegi elevati per installare le applicazioni gestite e utilizza il livello di privilegio dell'utente corrente per le applicazioni non gestite.<br/>                                                                                                                                                                                                      |
| [DisableMedia](disablemedia.md)<br/>                           | **REG \_ DWORD**<br/> | Se il criterio [DisableMedia](disablemedia.md) è impostato su "1", gli utenti e gli amministratori che eseguono un'installazione di manutenzione di un prodotto non possono utilizzare la finestra di dialogo Sfoglia per visualizzare le origini multimediali, ad esempio CD-ROM, per le origini di altri prodotti installabili. L'esplorazione di altri prodotti viene impedita indipendentemente dal fatto che l'installazione sia con privilegi elevati. È comunque possibile che l'utente reinstalli il prodotto da un supporto se l'utente dispone di un'origine multimediale correttamente etichettata.<br/> |
| [DisableRollback](disablerollback.md)<br/>                     | **REG \_ DWORD**<br/> | Se questo valore è impostato su "1", il programma di installazione non archivia i file di rollback durante l'installazione, disabilitando il rollback dell'installazione. Per impostazione predefinita, il rollback è abilitato. Si consiglia agli amministratori di non utilizzare questo criterio a meno che non sia assolutamente essenziale.<br/>                                                                                                                                                                                                                                                             |
| [SearchOrder](searchorder.md)<br/>                             | **REG \_ SZ**<br/>    | Ordine in cui il programma di installazione cerca i tre diversi tipi di origini:<br/> "n"-rete<br/> "m"-supporto (CD-ROM o DVD)<br/> "u"-URL (Uniform Resource Locator)<br/> Ad esempio, il valore "NMU" indica al programma di installazione di cercare prima le origini di rete, le origini supporti e le origini URL. Se si lascia una lettera, il tipo di volume corrispondente verrà rimosso dalla ricerca. In assenza di questo valore, l'ordine predefinito è la prima rete, quindi i supporti seguiti dall'URL.<br/>          |
| [Criteri di TransformsAtSource](transformsatsource-policy.md)<br/> | **REG \_ DWORD**<br/> | Se questo valore esiste ed è impostato su "1"; il programma di installazione cerca i file di trasformazione nella radice di tutte le origini di rete nell'oggetto di [**origine**](sourcelist.md) per il prodotto. Per impostazione predefinita, le trasformazioni vengono archiviate nella cartella Application Data del profilo di un utente.<br/>                                                                                                                                                                                                                                             |



 

 

 




