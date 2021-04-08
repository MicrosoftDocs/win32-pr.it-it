---
description: I provider implementano gli algoritmi di crittografia, generano chiavi, forniscono archiviazione chiavi e autenticano gli utenti. I provider possono essere implementati in hardware, software o entrambi.
ms.assetid: 42f76d22-1f0e-4e20-a19e-e5e926ab27f9
title: Informazioni sui provider di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11861b99dc8a19fc4300be2c9707462235f4a792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968062"
---
# <a name="understanding-cryptographic-providers"></a>Informazioni sui provider di crittografia

Il concetto di provider del servizio di crittografia introdotto nell'API di crittografia ([*CryptoAPI*](/windows/desktop/SecGloss/c-gly)) e che si è evoluto in qualche modo nell' [*API di crittografia: Next Generation*](/windows/desktop/SecGloss/c-gly) (CNG) è fondamentale per l'implementazione sicura della funzionalità di crittografia nei sistemi operativi Microsoft. Questi due SDK sono stati usati per creare molte applicazioni e vengono chiamati internamente da altri SDK. Ad esempio, Active Directory Servizi certificati e l'API di registrazione certificati si basano su CryptoAPI e CNG.

In generale, i provider implementano gli algoritmi di crittografia, generano chiavi, forniscono archiviazione chiavi e autenticano gli utenti. I provider possono essere implementati in hardware, software o entrambi. Le applicazioni compilate tramite CryptoAPI o CNG non possono modificare le chiavi create dai provider e non possono modificare l'implementazione dell'algoritmo crittografico. I provider multipli creati da Microsoft vengono distribuiti con i sistemi operativi. Altri provider sono stati creati e distribuiti da terze parti.

Negli argomenti seguenti vengono evidenziate le differenze tra i provider associati a CryptoAPI e quelli associati a CNG. Questa documentazione si riferisce in genere a provider senza riferimento all'SDK a cui sono associati, annotando l'associazione solo quando è pertinente.

-   [Provider del servizio di crittografia CryptoAPI](cryptoapi-cryptographic-service-providers.md)
-   [Provider di algoritmi di crittografia CNG](cng-cryptographic-algorithm-providers.md)
-   [Provider di archiviazione chiavi CNG](cng-key-storage-providers.md)
-   [Enumerazione dei provider installati](enumerating-installed-providers.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di registrazione certificati](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
