---
description: Quando un'applicazione usa il API Gestione credenziali per richiedere le credenziali, è previsto che l'utente immissione di informazioni che possono essere convalidate, dal sistema operativo o dall'applicazione.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formati dei nomi utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c2d4a31904e1cdc6c08da596e2db24054389387ef90142001e7f0e6e520567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915546"
---
# <a name="user-name-formats"></a>Formati dei nomi utente

Quando un'applicazione usa il API Gestione credenziali per richiedere le credenziali, è previsto che l'utente immissione di informazioni che possono essere convalidate, dal sistema operativo o dall'applicazione. L'utente può specificare le informazioni sulle credenziali di dominio in uno dei formati seguenti:

-   [Nome entità utente](#user-principal-name)
-   [Nome di accesso di livello inferiore](#down-level-logon-name)

## <a name="user-principal-name"></a>Nome entità utente

Il formato UPN [*(User Principal Name)*](../secgloss/u-gly.md) viene usato per specificare un nome di tipo Internet, ad esempio <b>UserName@Example.Microsoft.com</b> . La tabella seguente riepiloga le parti di un UPN.



| Parte                                                        | Esempio                                |
|-------------------------------------------------------------|----------------------------------------|
| Nome dell'account utente. Noto anche come nome di accesso.<br/> | *UserName*<br/>                  |
| Separatore. Valore letterale carattere, simbolo di at (@).<br/> | @<br/>                           |
| Suffisso UPN. Noto anche come nome di dominio.<br/>       | *Example.Microsoft.com* <br/> |



 

Un UPN può essere definito in modo implicito o esplicito. Un UPN implicito ha il formato <b>UserName@DNSDomainName.com</b> . Un UPN implicito è sempre associato all'account dell'utente, anche se non è definito un UPN esplicito. Un UPN esplicito ha il formato , in cui le stringhe di nome e suffisso vengono definite in modo esplicito <i><b>Name@Suffix</b></i> dall'amministratore.

## <a name="down-level-logon-name"></a>Down-Level di accesso

Il formato del nome di accesso di livello inferiore viene usato per specificare un dominio e un account utente in tale dominio, ad esempio <i><b>DOMAIN \\ UserName</b></i>. Nella tabella seguente sono riepilogate le parti di un nome di accesso di livello inferiore.



| Parte                                                           | Esempio               |
|----------------------------------------------------------------|-----------------------|
| Nome di dominio NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Separatore. Valore letterale carattere, barra rovesciata ( \\ ).<br/> | **\\**<br/>     |
| Nome dell'account utente. Noto anche come nome di accesso.<br/>    | *UserName*<br/> |



 

 

 
