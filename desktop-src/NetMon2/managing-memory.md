---
description: Se un esperto non riesce in fase di esecuzione, se si usano funzioni Network Monitor per la gestione della memoria, Network Monitor libera memoria allocata.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4cc5b38f5525b7c0d19e115c83ed9f770c72215c6b64825a089ec389bfc09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555881"
---
# <a name="managing-memory"></a>Gestione della memoria

Se un esperto non riesce in fase di esecuzione, se si usano funzioni Network Monitor per la gestione della memoria, Network Monitor libera memoria allocata. Tuttavia, quando si scrive un esperto, potrebbe essere necessario acquisire le risorse di sistema e le informazioni sulla struttura dei dati. Ad esempio, Network Monitor Protocol Coalesce Expert acquisisce un handle di file per compilare una nuova acquisizione. Ogni esperto deve creare la propria **gestione try/catch** in modo che l'esperto possa liberare le risorse acquisite.

Quando viene allocata memoria, usare le funzioni di memoria esistenti seguenti:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



