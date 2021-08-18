---
title: Integrità e privacy
description: Le comunicazioni client/servizio che richiedono l'autenticazione reciproca devono proteggere il traffico che scambiano dopo l'autenticazione.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- Integrità e privacy ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c287956fcebc250d5324a15f88fb6a47e087fca40f68f793dd695b47e6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187105"
---
# <a name="integrity-and-privacy"></a>Integrità e privacy

Le comunicazioni client/servizio che richiedono l'autenticazione reciproca devono proteggere il traffico che scambiano dopo l'autenticazione. Non è saggio eseguire l'autenticazione reciproca al momento della connessione iniziale al servizio se il traffico è successivamente soggetto a modifiche da parte di un utente non autorizzato. SSPI, RPC e COM forniscono utilità per la firma digitale e la crittografia dei messaggi. L'applicazione di firme digitali impedisce che il traffico modificato non sia rilevato e sconsiglia le intercettazioni. Naturalmente il traffico può essere intercettato, ma la decrittografia del traffico è sufficientemente difficile da dissuadere la maggior parte degli utenti non autorizzati.

A meno che i requisiti di prestazioni non siano gravi, è consigliabile usare sia la firma che la crittografia, in particolare per le funzioni amministrative. Anche quando le prestazioni sono un problema, alcuni clienti scelgono una sicurezza più rigida rispetto a prestazioni migliori. In questi casi, impostare opzioni configurabili per l'integrità e la privacy con maggiore sicurezza come opzione predefinita e prestazioni superiori.

I client RPC possono specificare il livello di integrità e privacy quando chiamano la [**funzione RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) per impostare i dati di autenticazione per l'associazione RPC. Usare **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** per la firma e **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** per la crittografia. Per altre informazioni, vedere [Autenticazione reciproca nelle applicazioni RPC](mutual-authentication-in-rpc-applications.md).

I servizi che usano un pacchetto SSPI per l'autenticazione reciproca possono eseguire query sul pacchetto per determinare se supporta le funzioni [**MakeSignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)e [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) per la firma e la crittografia dei messaggi. Per altre informazioni e un esempio di codice, vedere Garantire l'integrità della comunicazione [durante l'Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 