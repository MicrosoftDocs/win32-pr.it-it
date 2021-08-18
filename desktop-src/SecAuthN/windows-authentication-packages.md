---
description: Windows pacchetti di autenticazione forniscono servizi di autenticazione implementando funzionalità specifiche del pacchetto per le funzioni LsaLogonUser e LsaCallAuthenticationPackage fornite dall'LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Pacchetti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915080"
---
# <a name="windows-authentication-packages"></a>Windows Pacchetti di autenticazione

Windows pacchetti di autenticazione forniscono servizi di autenticazione implementando funzionalità specifiche del pacchetto per le funzioni [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) e [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fornite dall'LSA.

MSV1 \_ 0 è un esempio di un pacchetto Windows [*di autenticazione.*](../secgloss/a-gly.md) Il pacchetto MSV1 0 accetta un nome utente e una password con hash, che cerca nel database di Gestione account di \_ sicurezza (SAM). [](../secgloss/h-gly.md) [](../secgloss/s-gly.md) A seconda dei risultati della ricerca, il pacchetto di autenticazione MSV1 \_ 0 accetta o rifiuta il tentativo di autenticazione.

Per un elenco delle funzioni di supporto fornite da LSA Windows pacchetti di autenticazione che richiedono servizi di sistema, vedere [Funzioni LSA chiamate dai](authentication-functions.md)pacchetti di autenticazione .

Windows pacchetti di autenticazione devono implementare un set di funzioni chiamate dall'LSA. Per l'elenco completo delle funzioni, vedere [Funzioni implementate dai pacchetti di autenticazione](authentication-functions.md).

 

 
