---
description: Il motore di protocollo SSL (Schannel) utilizza un provider del servizio di crittografia (CSP) quando si eseguono operazioni di crittografia. Le applicazioni crittografiche possono chiamare CryptAcquireContext usando i \_ \_ provider SChannel di prova RSA SChannel e prova \_ DH \_ .
ms.assetid: ad1eabf1-23bc-4d23-8f8b-13f0bda95120
title: Uso di CSP Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289ed57d9f312ee1ef57aecf7534a8d585859126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308631"
---
# <a name="using-schannel-csps"></a>Uso di CSP Schannel

Il motore di protocollo SSL ([*Schannel*](../secgloss/s-gly.md)) utilizza un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) quando si eseguono operazioni di crittografia. Le applicazioni crittografiche possono chiamare [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) usando i \_ \_ provider SChannel di prova RSA SChannel e prova \_ DH \_ .

Questa sezione definisce i [*tipi CSP*](../secgloss/c-gly.md) RSA e Diffie-Hellman Schannel e descrive le funzionalità che un CSP deve supportare per essere compatibile con Schannel.dll, il motore del protocollo di crittografia. Un motore di protocollo è un programma che stabilisce un canale di comunicazione sicuro tra un'applicazione client e server.

Le applicazioni non devono tentare di usare le informazioni contenute in questa documentazione per usare la prova \_ RSA \_ Schannel o la dimostrazione \_ DH \_ Schannel direttamente. Questa documentazione spiega invece in che modo gli sviluppatori e i fornitori CSP devono scrivere CSP Schannel compatibili con i provider Microsoft Schannel.

Questa documentazione è concepita per aiutare gli sviluppatori CSP a implementare i CSP RSA o Diffie-Hellman Schannel compatibili. Si presuppone che gli sviluppatori abbiano familiarità con il protocollo SSL ( [*Secure Socket Layer*](../secgloss/s-gly.md) ) versione 3,0, crittografia a [*chiave pubblica*](../secgloss/p-gly.md) , [*certificati digitali*](../secgloss/d-gly.md)e il set di funzioni CryptoAPI. Per gli sviluppatori che hanno familiarità con questi argomenti si consiglia di leggere la specifica del protocollo SSL 3,0 e la documentazione di [Cryptography Essentials](cryptography-essentials.md) in questo SDK. Inoltre, gli sviluppatori RSA e Diffie-Hellman CSP devono essere a conoscenza delle specifiche del protocollo [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) insieme agli [*algoritmi RSA e Diffie-Hellman*](../secgloss/d-gly.md)pertinenti.

Per un esempio usato da un motore di protocollo Microsoft, vedere [creazione della chiave master](creating-the-master-key.md). Le chiamate alle funzioni di crittografia in questo esempio generano chiamate a funzioni CP che devono essere implementate da un CSP. Per scrivere un CSP compatibile, uno sviluppatore deve comprendere la specifica SSL 3,0 e combinare tali informazioni con una conoscenza del codice del motore di protocollo simile a quello usato in questo esempio.

Poiché è previsto che l'utilizzo del protocollo Private Communications Technology è minimo in futuro, gli sviluppatori di nuovi CSP non devono supportare questo protocollo. Il motore di protocollo Schannel lo supporta esclusivamente per la compatibilità con le versioni precedenti.

 

 
