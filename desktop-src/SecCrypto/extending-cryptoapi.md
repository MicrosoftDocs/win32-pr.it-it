---
description: CryptoAPI è stato progettato per essere facilmente estendibile. I nuovi tipi e parametri possono essere definiti da qualsiasi autore di provider del servizio di crittografia (CSP) per far in modo che CryptoAPI sia in grado di soddisfare i requisiti di un'ampia gamma di situazioni.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Estensione di CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0538e15f49e61dc26cacd4e81c42dd462aec092877428ebe865ab97c7729f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007020"
---
# <a name="extending-cryptoapi"></a>Estensione di CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) è stato progettato per essere facilmente estendibile. I nuovi tipi e parametri [](../secgloss/c-gly.md) possono essere definiti da qualsiasi autore di provider del servizio di crittografia (CSP) per far in modo che CryptoAPI sia in grado di soddisfare i requisiti di un'ampia gamma di situazioni.



| Elementi estensibili                                                                                                 | Commento                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipi di provider<br/>                                                                                        | Un tipo di provider rappresenta una famiglia o un tipo specifico di servizi di crittografia. È possibile definire nuovi tipi di provider, ognuno dei quali serve una particolare rete.<br/>                                                                                                                                                                                                                                                                                          |
| Parametri del provider<br/>                                                                                   | I parametri del provider vengono inviati e ricevuti [**rispettivamente tramite CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) e [**CPGetProvParam.**](https://www.bing.com/search?q=**CPGetProvParam**) I nuovi parametri del provider potrebbero consentire la configurazione di un CSP in modi non previsti dalle finestre di progettazione CryptoAPI.<br/>                                                                                                                                                                 |
| Identificatori di algoritmo<br/>                                                                                 | Le funzionalità di enumerazione di [**CPGetProvParam consentono alle applicazioni**](https://www.bing.com/search?q=**CPGetProvParam**) di elencare dinamicamente gli identificatori degli algoritmi. È [*possibile definire*](../secgloss/s-gly.md)nuovi [*algoritmi*](../secgloss/p-gly.md) [*simmetrici,*](../secgloss/h-gly.md) di chiave pubblica e hash in qualsiasi momento.<br/> |
| Tipi di coppia [*di chiavi pubblica/privata*](../secgloss/p-gly.md)<br/> | Anche se è possibile definire nuovi tipi di coppia di chiavi in base alle esigenze, attualmente vengono usate solo le coppie di chiavi di firma [*e*](../secgloss/e-gly.md) di scambio delle chiavi.<br/>                                                                                                                                                                                                                                           |
| Tipi DI BLOB chiave<br/>                                                                                        | I nuovi [*tipi di BLOB*](../secgloss/b-gly.md) di chiavi potrebbero consentire lo scambio flessibile di chiavi di sessione, chiavi pubbliche e coppie di chiavi pubblica/privata usando le funzioni [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) e [**CPImportKey.**](https://www.bing.com/search?q=**CPImportKey**)<br/>                                                                                                                                            |
| Parametri chiave<br/>                                                                                        | I parametri chiave vengono inviati e recuperati [**usando CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) e [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**). I nuovi parametri chiave potrebbero abilitare il supporto per molti tipi diversi di chiavi.<br/>                                                                                                                                                                                                                         |
| Parametri dell'oggetto hash<br/>                                                                                | I parametri dell'oggetto hash vengono inviati e recuperati [**usando CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) [**e CPGetHashParam.**](https://www.bing.com/search?q=**CPGetHashParam**) I nuovi parametri dell'oggetto hash potrebbero abilitare il supporto per molti tipi diversi [*di hash.*](../secgloss/h-gly.md)<br/>                                                                                                                                         |
| Valori dei flag<br/>                                                                                           | La maggior parte delle funzioni CryptoAPI/CryptoSPI ha *un parametro dwFlags.* I *nuovi valori dwFlags* potrebbero modificare il comportamento delle funzioni in base alle esigenze.<br/>                                                                                                                                                                                                                                                                                                       |



 

Le estensioni di CryptoAPI devono essere effettuate in modo responsabile. Prima di definire nuovi parametri e tipi di algoritmo, uno sviluppatore CSP deve consultare Microsoft Corporation, in modo che:

-   Le estensioni CryptoAPI comuni possono essere identificate e inserite nel file Wincrypt.h standard.
-   È possibile evitare conflitti tra spazi dei nomi.
-   È possibile determinare se l'estensione è necessaria o se è possibile eseguire una determinata operazione usando l'API corrente.

> [!Note]  
> Per essere compatibile con le applicazioni sviluppate per Microsoft Base Cryptographic Provider, un CSP deve supportare tutti gli elementi precedenti, come descritto in [Funzioni](cryptography-functions.md) di crittografia di base e [in](cryptography-functions.md)Funzioni del provider del servizio di crittografia .

 

 

 
