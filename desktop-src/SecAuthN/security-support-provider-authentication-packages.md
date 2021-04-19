---
description: Il sistema operativo Windows supporta l'autenticazione usando i pacchetti di sicurezza che funzionano sia come provider di supporto della sicurezza che come pacchetti di autenticazione.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Security Support Provider/pacchetti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4e7020f2d03b55631ee152cccc201791b645347
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311603"
---
# <a name="security-support-providerauthentication-packages"></a>Security Support Provider/pacchetti di autenticazione

Il sistema operativo Windows supporta l'autenticazione usando i [*pacchetti di sicurezza*](../secgloss/s-gly.md) che funzionano sia come provider di [*supporto della sicurezza*](../secgloss/s-gly.md) che come pacchetti di [*autenticazione*](../secgloss/a-gly.md). I pacchetti di sicurezza forniscono i servizi di supporto del processo di accesso di un pacchetto di autenticazione di Windows e forniscono servizi di autenticazione alle applicazioni implementando un set di funzioni di cui è stato eseguito il mapping all'interfaccia SSPI ( [Security Support Provider Interface](sspi.md) ).

Un pacchetto di sicurezza che funge da pacchetto di autenticazione e implementa la funzionalità richiesta da [*SSPI*](../secgloss/s-gly.md) è denominato pacchetto di Security Support Provider/autenticazione (SSP/AP).

Per ulteriori informazioni sui pacchetti di sicurezza, vedere [pacchetti SSP forniti da Microsoft](ssp-packages-provided-by-microsoft.md). Per informazioni sullo sviluppo di SSP/APs personalizzati, vedere [pacchetti di sicurezza personalizzati](custom-security-packages.md).

 

 
