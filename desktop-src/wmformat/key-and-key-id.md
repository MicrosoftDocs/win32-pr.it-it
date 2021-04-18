---
title: Chiave e ID chiave
description: Chiave e ID chiave
ms.assetid: 40618771-d601-4c31-8da9-5c649651f2f2
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Digital Rights Management (DRM), chiavi
- DRM (Digital Rights Management), chiavi
- Digital Rights Management (DRM), KID
- DRM (Digital Rights Management), KID
- ID chiave (KID)
- KID (ID chiave)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca7f74521fdf0f6cc268b8af1259f8468087f45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298141"
---
# <a name="key-and-key-id"></a>Chiave e ID chiave

Quando si crea il pacchetto di un file, si usa una chiave. Una chiave è una porzione di dati usati negli algoritmi di crittografia che proteggono il contenuto. Sono disponibili due parti per ogni chiave, ovvero un valore di inizializzazione della chiave di licenza e un ID chiave (spesso abbreviato come KID). L'ID chiave è pubblico e viene archiviato nell'intestazione del file come un modo per identificare la chiave necessaria per decrittografare il file. Il valore di inizializzazione chiave di licenza è un valore segreto che deve essere condiviso dal pacchetto di contenuto e dall'emittente della licenza.

Un ID chiave identifica il contenuto protetto dal punto di vista della licenza. Sebbene sia possibile utilizzare lo stesso ID chiave per più file, è consigliabile utilizzare sempre un ID chiave univoco per ogni parte del contenuto protetto.

Molti dei metodi descritti in questa documentazione usano le stringhe ID chiave per selezionare le licenze. Queste stringhe contengono l'ID chiave codificato in Base64.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](drmconcepts.md)
</dt> </dl>

 

 




