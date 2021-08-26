---
title: Chiave e ID chiave
description: Chiave e ID chiave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- digital rights management (DRM), chiavi
- DRM (Digital Rights Management),chiavi
- digital rights management (DRM),RIGHTS
- DRM (digital rights management),RIGHTS
- KEY ID (MAIUSC)
- KID (ID chiave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae448cd0c973ad11b55df6365039240ebe2c6ebadb3eda5f70b7f8dd1bfbfbc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929961"
---
# <a name="key-and-key-id"></a>Chiave e ID chiave

Quando si esegue il pacchetto di un file, si usa una chiave. Una chiave è un dato usato negli algoritmi di crittografia che proteggono il contenuto. Ogni chiave è in due parti: un valore di seed di chiave di licenza e un ID chiave (spesso abbreviato come TEMPOR). L'ID chiave è pubblico e viene archiviato nell'intestazione del file per identificare la chiave necessaria per decrittografare il file. Il valore di seed della chiave di licenza è un valore segreto che deve essere condiviso dall'autorità di creazione pacchetti del contenuto e dall'autorità emittente della licenza.

Un ID chiave identifica il contenuto protetto dal punto di vista della licenza. Sebbene sia possibile usare lo stesso ID chiave per più file, è consigliabile usare sempre un ID chiave univoco per ogni parte di contenuto protetto.

Molti dei metodi descritti in questa documentazione usano stringhe ID chiave per selezionare le licenze. Queste stringhe contengono l'ID chiave codificato in base64.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](drmconcepts.md)
</dt> </dl>

 

 




