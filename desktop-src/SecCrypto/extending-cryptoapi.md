---
description: CryptoAPI è stato progettato per essere facilmente estendibile. I nuovi tipi e parametri possono essere definiti da qualsiasi autore del provider del servizio di crittografia (CSP) per fare in modo che CryptoAPI si pieghi ai requisiti di un'ampia varietà di situazioni.
ms.assetid: fe87ccb8-16a3-443d-93df-0df02b8787f6
title: Estensione di CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62417f66b8a8bb2d06d145543f944f91868d366d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318235"
---
# <a name="extending-cryptoapi"></a>Estensione di CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) è stato progettato per essere facilmente estendibile. I nuovi tipi e parametri possono essere definiti da qualsiasi autore del [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per fare in modo che CryptoAPI si pieghi ai requisiti di un'ampia varietà di situazioni.



| Elementi estendibili                                                                                                 | Commento                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipi di provider<br/>                                                                                        | Un tipo di provider rappresenta una particolare famiglia o tipo di servizi di crittografia. È possibile definire nuovi tipi di provider, ognuno di essi che funge da nicchia particolare.<br/>                                                                                                                                                                                                                                                                                          |
| Parametri del provider<br/>                                                                                   | I parametri del provider vengono inviati e ricevuti rispettivamente usando [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) e [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**). I nuovi parametri del provider potrebbero consentire la configurazione di un CSP in modi non previsti dalle finestre di progettazione CryptoAPI.<br/>                                                                                                                                                                 |
| Identificatori di algoritmi<br/>                                                                                 | Le funzioni di enumerazione di [**CPGetProvParam**](https://www.bing.com/search?q=**CPGetProvParam**) consentono alle applicazioni di elencare in modo dinamico gli identificatori di algoritmi. È possibile definire nuovi algoritmi [*simmetrici*](../secgloss/s-gly.md), [*chiave pubblica*](../secgloss/p-gly.md)e [*hash*](../secgloss/h-gly.md) in qualsiasi momento.<br/> |
| Tipi di coppia di chiavi pubblica/[*privata*](../secgloss/p-gly.md)<br/> | Sebbene i nuovi tipi di coppia di chiavi possano essere definiti in base alle esigenze, vengono attualmente utilizzate solo [*coppie di chiavi*](../secgloss/e-gly.md) di firma e scambio di chiave.<br/>                                                                                                                                                                                                                                           |
| Tipi di BLOB di chiavi<br/>                                                                                        | I nuovi tipi di [*BLOB*](../secgloss/b-gly.md) chiave potrebbero consentire lo scambio di chiavi di sessione, chiavi pubbliche e coppie di chiavi pubbliche/private in modo flessibile usando le funzioni [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) e [**CPImportKey**](https://www.bing.com/search?q=**CPImportKey**) .<br/>                                                                                                                                            |
| Parametri chiave<br/>                                                                                        | I parametri chiave vengono inviati e recuperati usando [**CPSetKeyParam**](https://www.bing.com/search?q=**CPSetKeyParam**) e [**CPGetKeyParam**](https://www.bing.com/search?q=**CPGetKeyParam**). I nuovi parametri chiave potrebbero consentire il supporto per molti tipi diversi di chiavi.<br/>                                                                                                                                                                                                                         |
| Parametri dell'oggetto hash<br/>                                                                                | I parametri dell'oggetto hash vengono inviati e recuperati usando [**CPSetHashParam**](https://www.bing.com/search?q=**CPSetHashParam**) e [**CPGetHashParam**](https://www.bing.com/search?q=**CPGetHashParam**). I nuovi parametri dell'oggetto hash potrebbero consentire il supporto per molti tipi diversi di [*hash*](../secgloss/h-gly.md).<br/>                                                                                                                                         |
| Valori di flag<br/>                                                                                           | Per la maggior parte delle funzioni CryptoAPI/CryptoSPI è presente un parametro *dwFlags* . I nuovi valori *dwFlags* potrebbero modificare il comportamento delle funzioni secondo necessità.<br/>                                                                                                                                                                                                                                                                                                       |



 

Le estensioni per CryptoAPI devono essere eseguite in modo responsabile. Prima di definire nuovi parametri e tipi di algoritmi, uno sviluppatore CSP deve consultare Microsoft Corporation, in modo che:

-   Le estensioni CryptoAPI comuni possono essere identificate e inserite nel file Wincrypt. h standard.
-   È possibile evitare conflitti tra gli spazi dei nomi.
-   È possibile determinare se l'estensione è obbligatoria o se è possibile ottenere una determinata operazione usando l'API corrente.

> [!Note]  
> Per la compatibilità di un CSP con le applicazioni sviluppate per il provider del servizio di crittografia di base Microsoft, deve supportare tutti gli elementi precedenti, come descritto in funzioni di [crittografia di base](cryptography-functions.md) e in funzioni del provider del [servizio di crittografia](cryptography-functions.md).

 

 

 
