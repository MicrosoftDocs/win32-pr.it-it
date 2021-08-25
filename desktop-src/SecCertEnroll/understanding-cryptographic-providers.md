---
description: I provider implementano algoritmi di crittografia, generano chiavi, forniscono l'archiviazione delle chiavi e autenticano gli utenti. I provider possono essere implementati in hardware, software o entrambi.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Informazioni sui provider di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f167f186ed4da1ac5e97aba8a3c4659f13f29f253de3f489981fc6b32810015f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127221"
---
# <a name="understanding-cryptographic-providers"></a>Informazioni sui provider di crittografia

Il concetto di provider di crittografia introdotto nell'API di crittografia ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) e che si è evoluto in qualche modo nell'API di [*crittografia:*](/windows/desktop/SecGloss/c-gly) Next Generation (CNG) è fondamentale per l'implementazione sicura della funzionalità di crittografia nei sistemi operativi Microsoft. Questi due SDK sono stati usati per creare molte applicazioni e vengono chiamati internamente da altri SDK. Ad esempio, Servizi certificati Active Directory'API di registrazione certificati si basano su CryptoAPI e CNG.

In generale, i provider implementano algoritmi di crittografia, generano chiavi, forniscono l'archiviazione delle chiavi e autenticano gli utenti. I provider possono essere implementati in hardware, software o entrambi. Le applicazioni compilate con CryptoAPI o CNG non possono modificare le chiavi create dai provider e non possono modificare l'implementazione dell'algoritmo di crittografia. I più provider creati da Microsoft vengono distribuiti con i sistemi operativi. Altri provider sono stati creati e distribuiti da terze parti.

Negli argomenti seguenti vengono evidenziate le differenze tra i provider associati a CryptoAPI e quelli associati a CNG. In genere, questa documentazione si riferisce ai provider senza riferimento all'SDK a cui sono associati, notando l'associazione solo quando è pertinente.

-   [Provider del servizio di crittografia CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Provider di algoritmi di crittografia CNG](cng-cryptographic-algorithm-providers.md)
-   [Provider di Archiviazione CNG](cng-key-storage-providers.md)
-   [Enumerazione dei provider installati](enumerating-installed-providers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
