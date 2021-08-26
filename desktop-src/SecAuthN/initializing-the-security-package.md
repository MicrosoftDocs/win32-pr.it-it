---
description: Elenca e illustra i passaggi necessari per inizializzare un pacchetto di sicurezza.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inizializzazione del pacchetto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d39cbbd9a1126a22d04c14bee3b6ac9b305b2feb3593d03756779e4cb0649b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015851"
---
# <a name="initializing-the-security-package"></a>Inizializzazione del pacchetto di sicurezza

Questi passaggi sono necessari prima di usare SSPI:

1.  La funzione di inizializzazione deve essere chiamata per ottenere l'indirizzo della tabella delle funzioni di sicurezza.

    Il client e il server chiamano [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) per un puntatore a una tabella di distribuzione [**SecurityFunctionTable.**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) Questa tabella contiene puntatori alle funzioni di callback dichiarate in Sspi.h. Questi puntatori forniscono l'accesso alle implementazioni della DLL delle varie funzioni SSPI.

2.  È necessario ottenere informazioni sui pacchetti di sicurezza supportati.

    Sebbene la maggior parte delle applicazioni usi pacchetti di sicurezza che supportano funzionalità predefinite o comuni, i pacchetti di sicurezza possono avere funzionalità univoche di interesse per l'applicazione. Un'applicazione che ha bisogno di funzionalità speciali può usare un pacchetto che offre tali funzionalità. Per altre informazioni, vedere [Recupero di informazioni sui pacchetti di sicurezza](getting-information-about-security-packages.md).

A questo punto, l'applicazione ha inizializzato correttamente un provider di servizi condivisi e ha scelto un pacchetto di sicurezza con funzionalità sufficienti.

Il [*pacchetto Negotiate*](../secgloss/n-gly.md) può essere usato quando [](../secgloss/s-gly.md) l'accordo tra client e server sul pacchetto di sicurezza da usare viene eseguito in background. Se il pacchetto Negotiate non viene usato, il client e il server devono accettare il pacchetto di sicurezza specifico da usare prima di eseguire la procedura di installazione precedente.

 

 
