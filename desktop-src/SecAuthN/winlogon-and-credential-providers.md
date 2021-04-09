---
description: È il modulo Windows che esegue l'accesso interattivo per una sessione di accesso. Il comportamento di Winlogon può essere personalizzato implementando e registrando un provider di credenziali.
ms.assetid: 6721367b-e200-4297-897b-4772226203b0
title: Provider di credenziali e Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce72e533f7cee6bc89bc2f995b94b7881448734d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966621"
---
# <a name="winlogon-and-credential-providers"></a>Provider di credenziali e Winlogon

[*Winlogon*](../secgloss/w-gly.md) è il modulo Windows che esegue l'accesso interattivo per una [*sessione di accesso*](../secgloss/l-gly.md). Il comportamento di Winlogon può essere personalizzato implementando e registrando un provider di credenziali.

Per informazioni sull'implementazione di un provider di credenziali, vedere gli argomenti seguenti.



| Argomento                                                                                                           | Descrizione                                                                                            |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Esperienza di accesso di Windows basata su provider di credenziali](https://go.microsoft.com/fwlink/?LinkId=717287)<br/> | Panoramica dell'architettura di Winlogon e del provider di credenziali e di un provider di credenziali di esempio.<br/> |
| [Interfacce della shell](../shell/samples-usingthumbnailproviders.md)<br/>                                                                | Riferimento all'interfaccia del provider di credenziali.<br/>                                                    |
| [Provider di credenziali in Windows 10](credential-providers-in-windows.md)<br/>                            | Provider di credenziali di terze parti e provider di credenziali di sistema in Windows 10.<br/>             |



 

Per un'implementazione del provider di credenziali di esempio, vedere l'esempio che si trova nella directory di installazione di Windows SDK in \\ esempi di \\ sicurezza \\ CredentialProvider.

**Windows Server 2003 e Windows XP:** I provider di credenziali non sono supportati. Per informazioni sulla personalizzazione di Winlogon, vedere [Winlogon e Gina](winlogon-and-gina.md).

 

 
