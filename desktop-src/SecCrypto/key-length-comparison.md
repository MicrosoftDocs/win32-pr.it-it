---
description: Microsoft Enhanced Cryptographic Provider offre un'applicazione con sicurezza più avanzata rispetto a quella attualmente disponibile con Microsoft Base Cryptographic Provider. Una maggiore lunghezza della chiave offre agli utenti maggiore protezione per i dati sensibili.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Confronto della lunghezza della chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65615f6ffb9679b922600c4617e401067d565ac7dd62a258ae07a757d2cec7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622346"
---
# <a name="key-length-comparison"></a>Confronto della lunghezza della chiave

Microsoft Enhanced Cryptographic Provider offre un'applicazione con sicurezza più avanzata rispetto a quella attualmente disponibile con Microsoft Base Cryptographic Provider. Una maggiore lunghezza della chiave offre agli utenti maggiore protezione per i dati sensibili.

Nella tabella seguente sono elencate le [*lunghezze di chiave predefinite*](../secgloss/k-gly.md) supportate dal provider di base e dal provider avanzato per gli algoritmi standard.



| Algoritmo                                                                                | Base Provider | Provider forti e migliorati |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Chiave RSA Exchange                                                                         | 512 bit       | 1.024 bit                     |
| Firma RSA                                                                            | 512 bit       | 1.024 bit                     |
| RC2                                                                                      | 40 bit        | 128 bit                       |
| RC4                                                                                      | 40 bit        | 128 bit                       |
| DES                                                                                      | Non supportato | 56 bit                        |
| [*Triple DES*](../secgloss/t-gly.md) (2 chiavi) | Non supportato | 112 bit                       |
| Triple DES (3 chiavi)                                                                       | Non supportato | 168 bit                       |



 

[*Gli*](../secgloss/d-gly.md) algoritmi [*DES e Triple DES*](../secgloss/t-gly.md) sono supportati nel provider avanzato.

Il provider avanzato è compatibile con le versioni precedenti con il provider di base distribuito con le versioni precedenti di CryptoAPI con l'eccezione seguente. Sia il provider di base che il provider avanzato possono generare solo chiavi di sessione di lunghezza della chiave predefinita. La lunghezza predefinita delle chiavi di sessione per il provider di base è di 40 bit. La lunghezza predefinita della chiave per il provider avanzato è di 128 bit. Il provider avanzato non può creare chiavi con lunghezze di chiave compatibili con il provider di base. Tuttavia, il provider avanzato può importare lunghezze di chiave di qualsiasi dimensione, fino a 128 bit.

 

 
