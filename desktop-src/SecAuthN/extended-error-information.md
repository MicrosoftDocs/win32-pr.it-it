---
description: Alcuni pacchetti di sicurezza supportano messaggi di errore estesi che consentono ai lati di un collegamento di comunicazione di comunicare i motivi di un errore.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Informazioni sugli errori estesi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd93de1691a01802f65397abb1607612f5b7e61a311c9f801854a00c1ab4f05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008219"
---
# <a name="extended-error-information"></a>Informazioni sugli errori estesi

Alcuni [*pacchetti di sicurezza*](/windows/desktop/SecGloss/s-gly) supportano messaggi di errore estesi che consentono ai lati di un collegamento di comunicazione di comunicare i motivi di un errore. Ad esempio, il [*protocollo Kerberos*](/windows/desktop/SecGloss/k-gly) potrebbe non riuscire a causa di una discrepanza temporale tra l'ora della richiesta di un ticket Kerberos e l'ora del problema del ticket. Con le informazioni restituite dalle informazioni sugli errori estesi, un client può risincronizzare l'orologio e generare un nuovo messaggio di connessione.

Un pacchetto di sicurezza che imposta il flag SECPKG FLAG EXTENDED ERROR nel membro fCapabilities di una \_ \_ struttura \_ [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa)  indica che il pacchetto di sicurezza supporta messaggi di errore estesi.

Le applicazioni client che richiedono messaggi di errore estesi specificano il flag ISC REQ EXTENDED ERROR quando \_ si chiama la funzione \_ \_ [**InitializeSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Le applicazioni server che richiedono messaggi di errore estesi impostano il flag ASC \_ REQ \_ EXTENDED ERROR quando si \_ chiama [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

 

 
