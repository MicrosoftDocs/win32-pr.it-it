---
description: Se un esperto non riesce in fase di esecuzione, se si usano Network Monitor funzioni per la gestione della memoria, Network Monitor libera la memoria allocata.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966773"
---
# <a name="managing-memory"></a>Gestione della memoria

Se un esperto non riesce in fase di esecuzione, se si usano Network Monitor funzioni per la gestione della memoria, Network Monitor libera la memoria allocata. Tuttavia, quando si scrive un esperto, potrebbe essere necessario acquisire le risorse di sistema e le informazioni sulla struttura dei dati. Ad esempio, l'esperto di COALESCE del protocollo Network Monitor acquisisce un handle di file per compilare una nuova acquisizione. Ogni esperto deve creare una propria gestione **try/catch** in modo che l'esperto possa liberare risorse acquisite.

Quando la memoria viene allocata, usare le funzioni di memoria esistenti seguenti:

-   [**ExpertAllocMemory**](expertallocmemory.md)
-   [**ExpertReallocMemory**](expertreallocmemory.md)

 

 



