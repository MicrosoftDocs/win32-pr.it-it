---
description: Quando un'applicazione usa l'API di gestione delle credenziali per richiedere le credenziali, è previsto che l'utente immetta le informazioni che possono essere convalidate dal sistema operativo o dall'applicazione.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formati di nome utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315856"
---
# <a name="user-name-formats"></a>Formati di nome utente

Quando un'applicazione usa l'API di gestione delle credenziali per richiedere le credenziali, è previsto che l'utente immetta le informazioni che possono essere convalidate dal sistema operativo o dall'applicazione. L'utente può specificare le informazioni sulle credenziali di dominio in uno dei formati seguenti:

-   [Nome entità utente](#user-principal-name)
-   [Nome di accesso di livello inferiore](#down-level-logon-name)

## <a name="user-principal-name"></a>Nome entità utente

Il formato del [*nome dell'entità utente*](../secgloss/u-gly.md) (UPN) viene usato per specificare un nome di tipo Internet, ad esempio <b>UserName@Example.Microsoft.com</b> . Nella tabella seguente sono riepilogate le parti di un UPN.



| Parte                                                        | Esempio                                |
|-------------------------------------------------------------|----------------------------------------|
| Nome dell'account utente. Noto anche come nome di accesso.<br/> | *UserName*<br/>                  |
| Separatore. Valore letterale carattere, il simbolo di chiocciola (@).<br/> | @<br/>                           |
| Suffisso UPN. Noto anche come nome di dominio.<br/>       | *Example.Microsoft.com* <br/> |



 

Un UPN può essere definito in modo implicito o esplicito. Un UPN implicito è nel formato <b>UserName@DNSDomainName.com</b> . Un UPN implicito è sempre associato all'account dell'utente, anche se non è definito un UPN esplicito. Un UPN esplicito è nel formato <i><b>Name@Suffix</b></i> , in cui le stringhe nome e suffisso sono definite in modo esplicito dall'amministratore.

## <a name="down-level-logon-name"></a>Nome di accesso Down-Level

Il formato del nome di accesso di livello inferiore viene usato per specificare un dominio e un account utente in tale dominio, ad esempio <i><b>dominio \\ username</b></i>. Nella tabella seguente sono riepilogate le parti di un nome di accesso di livello inferiore.



| Parte                                                           | Esempio               |
|----------------------------------------------------------------|-----------------------|
| Nome di dominio NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Separatore. Valore letterale carattere, barra rovesciata ( \\ ).<br/> | **\\**<br/>     |
| Nome dell'account utente. Noto anche come nome di accesso.<br/>    | *UserName*<br/> |



 

 

 
