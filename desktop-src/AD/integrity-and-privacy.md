---
title: Integrità e privacy
description: Le comunicazioni client/servizi che richiedono l'autenticazione reciproca devono proteggere il traffico scambiato dopo l'autenticazione.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- Integrità e privacy AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ed167c3796aec2b0717b1207ff56565ec94afa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956317"
---
# <a name="integrity-and-privacy"></a>Integrità e privacy

Le comunicazioni client/servizi che richiedono l'autenticazione reciproca devono proteggere il traffico scambiato dopo l'autenticazione. Non è consigliabile eseguire l'autenticazione reciproca al momento della connessione iniziale al servizio se il traffico è successivamente soggetto a modifiche da parte di un utente non autorizzato. SSPI, RPC e COM forniscono tutte le utilità per la firma digitale e la crittografia dei messaggi. L'applicazione di firme digitali impedisce che il traffico modificato non venga rilevato e sconsiglia l'intercettazione. Il traffico può essere intercettato naturalmente, ma la decrittografia del traffico è abbastanza complessa da scoraggiare la maggior parte degli utenti non autorizzati.

A meno che i requisiti di prestazioni non siano gravi, è consigliabile usare sia la firma che la crittografia, in particolare per le funzioni amministrative. Anche quando le prestazioni sono un problema, alcuni clienti scelgono una sicurezza più stretta rispetto alle prestazioni migliori. In questi casi, rendere le opzioni configurabili per l'integrità e la privacy con una protezione più elevata, l'opzione predefinita e le prestazioni più elevate.

I client RPC possono specificare il livello di integrità e privacy quando chiamano la funzione [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) per impostare i dati di autenticazione per l'associazione RPC. Usare **l' \_ \_ \_ \_ \_ integrità PKT del livello auth c RPC** per la firma e il **livello di \_ autenticazione RPC c \_ \_ \_ PKT \_ privacy** per la crittografia. Per ulteriori informazioni, vedere [l'autenticazione reciproca nelle applicazioni RPC](mutual-authentication-in-rpc-applications.md).

I servizi che utilizzano un pacchetto SSPI per l'autenticazione reciproca possono eseguire query sul pacchetto per determinare se supporta le funzioni [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) per la firma e la crittografia dei messaggi. Per ulteriori informazioni e un esempio di codice, vedere [garantire l'integrità della comunicazione durante lo scambio di messaggi](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 