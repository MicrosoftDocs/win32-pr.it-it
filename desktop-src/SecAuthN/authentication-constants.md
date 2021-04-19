---
description: Elenca le costanti usate per le API di autenticazione Microsoft.
ms.assetid: 3e5b7fd8-01bf-4090-b68f-006b7e2228a9
title: Costanti di autenticazione (autenticazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d671f356f11ccaf1f5aece1dc1168d3106d578c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316233"
---
# <a name="authentication-constants-authentication"></a>Costanti di autenticazione (autenticazione)

## <a name="credentials-management-constants"></a>Costanti di gestione delle credenziali

Gestione credenziali usa le costanti seguenti per specificare le dimensioni massime delle stringhe.



| Costante                                        | Descrizione                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| \_lunghezza massima \_ messaggi \_ CREDUI<br/>         | Numero massimo di caratteri per il membro **pszMessageText** di una struttura di [**\_ informazioni CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| \_ \_ lunghezza didascalia massima CREDUI \_<br/>         | Numero massimo di caratteri per il membro **pszCaptionText** di una struttura di [**\_ informazioni CREDUI**](/windows/desktop/api/WinCred/ns-wincred-credui_infoa) .<br/> |
| \_lunghezza di \_ destinazione generica CREDUI Max \_ \_<br/> | Numero massimo di caratteri in una stringa che specifica un nome di destinazione.<br/>                                             |
| \_lunghezza massima \_ \_ destinazione dominio \_ CREDUI<br/>  | Numero massimo di caratteri in una stringa che specifica un nome di dominio.<br/>                                             |
| \_lunghezza max \_ nome utente \_ CREDUI<br/>        | Numero massimo di caratteri in una stringa che specifica il nome di un account utente.<br/>                                       |
| \_lunghezza massima \_ password \_ CREDUI<br/>        | Numero massimo di caratteri in una stringa che specifica una password.<br/>                                                |



 

## <a name="gina-defined-values"></a>Valori definiti da Gina

Le funzioni di interfaccia [*Gina*](/windows/desktop/SecGloss/g-gly) e le funzioni di supporto [*Winlogon*](/windows/desktop/SecGloss/w-gly) utilizzano i valori definiti seguenti.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 



| Valore                                                              | Descrizione                                                                                                                          |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**\_opzione di accesso wlx \_ \_ xxx**](wlx-logon-option-xxx.md)<br/> | Contiene opzioni di accesso predefinite. Viene usato dal parametro *dwOptions* di [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).<br/> |
| [**WLX \_ SAS \_ tipo \_ xxx**](wlx-sas-type-xxx.md)<br/>         | Definisce un tipo di firma di accesso condiviso specifico.<br/>                                                                                              |



 

 

