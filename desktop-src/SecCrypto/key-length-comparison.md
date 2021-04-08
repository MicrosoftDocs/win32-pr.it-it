---
description: Microsoft Enhanced Cryptographic Provider fornisce un'applicazione con una sicurezza più avanzata rispetto a quella attualmente disponibile con il provider di crittografia di base Microsoft. Una maggiore lunghezza della chiave offre agli utenti maggiore protezione per i dati sensibili.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Confronto Lunghezza chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885657"
---
# <a name="key-length-comparison"></a>Confronto Lunghezza chiave

Microsoft Enhanced Cryptographic Provider fornisce un'applicazione con una sicurezza più avanzata rispetto a quella attualmente disponibile con il provider di crittografia di base Microsoft. Una maggiore lunghezza della chiave offre agli utenti maggiore protezione per i dati sensibili.

La tabella seguente elenca le [*lunghezze di chiave*](../secgloss/k-gly.md) predefinite supportate dal provider di base e il provider avanzato per gli algoritmi standard.



| Algoritmo                                                                                | Provider di base | Provider avanzati e avanzati |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Scambio di chiavi RSA                                                                         | 512 bit       | 1.024 bit                     |
| Firma RSA                                                                            | 512 bit       | 1.024 bit                     |
| RC2                                                                                      | 40 bit        | 128 bit                       |
| RC4                                                                                      | 40 bit        | 128 bit                       |
| DES                                                                                      | Non supportato | 56 bit                        |
| [*Triple des*](../secgloss/t-gly.md) (2 chiavi) | Non supportato | 112 bit                       |
| Triple DES (3 chiavi)                                                                       | Non supportato | 168 bit                       |



 

Gli algoritmi [*des e*](../secgloss/d-gly.md) [*triple des*](../secgloss/t-gly.md) sono supportati nel provider migliorato.

Il provider avanzato è compatibile con le versioni precedenti del provider di base distribuito con le versioni precedenti di CryptoAPI con la seguente eccezione. Sia il provider di base che il provider avanzato possono generare solo chiavi di sessione con la lunghezza della chiave predefinita. La lunghezza predefinita delle chiavi di sessione per il provider di base è 40 bit. La lunghezza della chiave predefinita per il provider avanzato è 128 bit. Il provider avanzato non può creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider avanzato può importare lunghezze di chiave di qualsiasi dimensione, fino a 128 bit.

 

 
