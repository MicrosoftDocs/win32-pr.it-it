---
title: Punti di sincronizzazione
description: Quando i set di proprietà sono supportati nello stesso oggetto di IStorage, è importante conoscere i punti di sincronizzazione tra l'archiviazione di base e l'archiviazione delle proprietà.
ms.assetid: 34cc4338-b29f-43f9-946d-14b2b235ccec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf924458d81003e2cc211ff810ebb714399ac28e91189586491b584cff6a3390
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034881"
---
# <a name="synchronization-points"></a>Punti di sincronizzazione

Quando i set di proprietà sono supportati nello stesso oggetto di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), è importante conoscere i punti di sincronizzazione tra l'archiviazione di base e l'archiviazione delle proprietà.

L'archiviazione del set di proprietà contiene il flusso del set di proprietà in un buffer interno fino a quando non viene eseguito il commit del buffer [**tramite il metodo IPropertyStorage::Commit.**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) Questo vale se [**IPropertyStorage è**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) stato aperto in modalità transazione o in modalità diretta.

 

 




