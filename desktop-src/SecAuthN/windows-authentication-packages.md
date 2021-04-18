---
description: I pacchetti di autenticazione di Windows forniscono servizi di autenticazione implementando funzionalità specifiche del pacchetto per le funzioni LsaLogonUser e LsaCallAuthenticationPackage fornite da LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Pacchetti di autenticazione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525843"
---
# <a name="windows-authentication-packages"></a>Pacchetti di autenticazione di Windows

I pacchetti di autenticazione di Windows forniscono servizi di autenticazione implementando funzionalità specifiche del pacchetto per le funzioni [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) e [**LSACALLAUTHENTICATIONPACKAGE**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fornite da LSA.

MSV1 \_ 0 è un esempio di pacchetto di [*autenticazione*](../secgloss/a-gly.md)di Windows. Il \_ pacchetto MSV1 0 accetta un nome utente e una password con [*hash*](../secgloss/h-gly.md) , che cerca nel database [*Gestione account di sicurezza*](../secgloss/s-gly.md) (Sam). A seconda dei risultati della ricerca, il \_ pacchetto di autenticazione MSV1 0 accetta o rifiuta il tentativo di autenticazione.

Per un elenco delle funzioni di supporto che LSA fornisce per l'uso da parte dei pacchetti di autenticazione di Windows che richiedono i servizi di sistema, vedere [funzioni LSA chiamate dai pacchetti di autenticazione](authentication-functions.md).

I pacchetti di autenticazione di Windows devono implementare un set di funzioni chiamate da LSA. Per l'elenco completo delle funzioni, vedere [funzioni implementate dai pacchetti di autenticazione](authentication-functions.md).

 

 
