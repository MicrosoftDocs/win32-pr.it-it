---
description: Modulo di Windows che esegue l'accesso interattivo per una sessione di accesso. Il comportamento di Winlogon può essere personalizzato implementando e registrando un Provider di credenziali.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Winlogon e provider di credenziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5a110c741289de9fdd08f1f5d5c820e9695f057b1d74db2e56f014f5da28eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785771"
---
# <a name="winlogon-and-credential-providers"></a>Winlogon e provider di credenziali

[*Winlogon è il*](../secgloss/w-gly.md) modulo Windows che esegue l'accesso interattivo per una [*sessione di accesso*](../secgloss/l-gly.md). Il comportamento di Winlogon può essere personalizzato implementando e registrando un Provider di credenziali.

Per informazioni sull'implementazione di Provider di credenziali, vedere gli argomenti seguenti.



| Argomento                                                                                                           | Descrizione                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Provider di credenziali'accesso Windows guidata dall'utente](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Panoramica dell'architettura winlogon Provider di credenziali e di un esempio Provider di credenziali.<br/> |
| [Interfacce della shell](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Provider di credenziali riferimento all'interfaccia.<br/>                                                    |
| [Provider di credenziali in Windows 10](credential-providers-in-windows.md)<br/>                            | Provider di credenziali di terze parti e provider di credenziali di sistema Windows 10.<br/>             |



 

Per un esempio di Provider di credenziali, vedere l'esempio disponibile nella directory di installazione di Windows SDK in \\ Samples \\ Security CredentialProvider (Esempi di \\ CredentialProvider di sicurezza).

**Windows Server 2003 e Windows XP:** I provider di credenziali non sono supportati. Per informazioni sulla personalizzazione di Winlogon, vedere [Winlogon e LANA.](winlogon-and-gina.md)

 

 
