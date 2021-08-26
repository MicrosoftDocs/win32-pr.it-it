---
description: Importante Questa API è deprecata.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7ef58122e47594b195700241b936b8985cd88137c52841976495b195d7e4c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876191"
---
# <a name="cryptographic-service-providers"></a>Provider del servizio di crittografia

> [!IMPORTANT]
> Questa API è deprecata. Il software nuovo ed esistente deve iniziare [a Cryptography Next Generation api.](/windows/desktop/SecCNG/cng-portal) Microsoft potrà rimuovere questa API nelle versioni future.

 

Un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) contiene implementazioni di standard e algoritmi di crittografia. Come minimo, un CSP è costituito da una libreria a [*collegamento*](../secgloss/d-gly.md) dinamico (DLL) che implementa le funzioni in [*CryptoSPI*](../secgloss/c-gly.md) (un'interfaccia [*del programma di sistema*](../secgloss/s-gly.md)). La maggior parte dei CSP contiene l'implementazione di tutte le proprie funzioni. Alcuni provider di servizi cloud, tuttavia, implementano le funzioni principalmente in un programma di servizio basato Windows-based gestito dal Windows di controllo del servizio. Altri implementano funzioni nell'hardware, ad esempio un [*smart card*](../secgloss/s-gly.md) o un coprocessore sicuro. Se un CSP non implementa le proprie funzioni, la DLL funge da livello pass-through, facilitando la comunicazione tra il sistema operativo e l'implementazione CSP effettiva.

Questa sezione include gli argomenti seguenti.



| Argomento                                                                                      | Contenuto                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Tipi di provider del servizio di crittografia](cryptographic-provider-types.md)                           | I tipi di provider del servizio di crittografia sono famiglie di provider di servizi di crittografia che condividono formati di dati e protocolli di crittografia. I formati di dati includono gli schemi [*di riempimento*](../secgloss/p-gly.md) degli [*algoritmi, le lunghezze delle*](../secgloss/k-gly.md)chiavi e le modalità predefinite. |
| [Provider del servizio di crittografia Microsoft](microsoft-cryptographic-service-providers.md) | Informazioni dettagliate sui CSP attualmente disponibili da Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
