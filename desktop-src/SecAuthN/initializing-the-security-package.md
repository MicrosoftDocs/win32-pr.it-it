---
description: Elenca e illustra i passaggi necessari per inizializzare un pacchetto di sicurezza.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Inizializzazione del pacchetto di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131182"
---
# <a name="initializing-the-security-package"></a>Inizializzazione del pacchetto di sicurezza

Questi passaggi sono necessari prima di utilizzare SSPI:

1.  La funzione di inizializzazione deve essere chiamata per ottenere l'indirizzo della tabella delle funzioni di sicurezza.

    Il client e il server chiamano [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) per un puntatore a una tabella di invio [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) . Questa tabella contiene i puntatori alle funzioni di callback dichiarate in SSPI. h. Questi puntatori forniscono l'accesso alle implementazioni della DLL delle varie funzioni SSPI.

2.  È necessario ottenere informazioni sui pacchetti di sicurezza supportati.

    Sebbene la maggior parte delle applicazioni usi pacchetti di sicurezza che supportano le funzionalità predefinite o comuni, i pacchetti di sicurezza possono avere funzionalità univoche di interesse per l'applicazione. Un'applicazione che necessita di funzionalità speciali può usare un pacchetto che offre tali funzionalità. Per ulteriori informazioni, vedere [ottenere informazioni sui pacchetti di sicurezza](getting-information-about-security-packages.md).

A questo punto, l'applicazione ha inizializzato correttamente un SSP e ha scelto un pacchetto di sicurezza con funzionalità sufficienti.

Il pacchetto [*Negotiate*](../secgloss/n-gly.md) può essere usato in caso di accordo tra il client e il server in cui viene eseguito il [*pacchetto di sicurezza*](../secgloss/s-gly.md) da usare. Se il pacchetto Negotiate non viene utilizzato, il client e il server devono accettare il pacchetto di sicurezza specifico da utilizzare prima di eseguire i passaggi di configurazione descritti in precedenza.

 

 
