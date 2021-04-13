---
description: Importante questa API è deprecata.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401653"
---
# <a name="cryptographic-service-providers"></a>Provider del servizio di crittografia

> [!IMPORTANT]
> Questa API è deprecata. Il software nuovo ed esistente dovrebbe iniziare a usare le [API di prossima generazione di crittografia.](/windows/desktop/SecCNG/cng-portal) Microsoft può rimuovere questa API nelle versioni future.

 

Un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) contiene implementazioni di algoritmi e standard crittografici. Come minimo, un CSP è costituito da una [*libreria di collegamento dinamico*](../secgloss/d-gly.md) (dll) che implementa le funzioni in [*CryptoSPI*](../secgloss/c-gly.md) (un'interfaccia del [*programma di sistema*](../secgloss/s-gly.md)). La maggior parte dei CSP contiene l'implementazione di tutte le relative funzioni. Alcuni CSP, tuttavia, implementano le proprie funzioni principalmente in un programma di servizio basato su Windows gestito da Gestione controllo servizi di Windows. Altri implementano funzioni in hardware, ad esempio una [*Smart Card*](../secgloss/s-gly.md) o un coprocessore protetto. Se un CSP non implementa funzioni proprie, la DLL funge da livello pass-through, facilitando la comunicazione tra il sistema operativo e l'implementazione effettiva di CSP.

Questa sezione include gli argomenti seguenti.



| Argomento                                                                                      | Contenuto                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipi di provider di crittografia](cryptographic-provider-types.md)                           | I tipi di provider del servizio di crittografia sono famiglie di provider di servizi di crittografia che condividono formati di dati e protocolli crittografici. I formati di dati includono schemi di [*riempimento*](../secgloss/p-gly.md) degli algoritmi, [*lunghezze delle chiavi*](../secgloss/k-gly.md)e modalità predefinite. |
| [Provider del servizio di crittografia Microsoft](microsoft-cryptographic-service-providers.md) | Informazioni dettagliate sui CSP attualmente disponibili da Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
