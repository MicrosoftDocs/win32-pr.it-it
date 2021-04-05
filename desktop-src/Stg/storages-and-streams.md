---
title: Archiviazione e flussi
description: Un oggetto di archiviazione è analogo a una directory file system.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708353"
---
# <a name="storages-and-streams"></a>Archiviazione e flussi

Un oggetto di archiviazione è analogo a una directory file system. Così come una directory può contenere altre directory e file, un oggetto di archiviazione può contenere altri oggetti di archiviazione e oggetti Stream. Analogamente a una directory, un oggetto di archiviazione tiene traccia delle posizioni e delle dimensioni degli oggetti di archiviazione e degli oggetti flusso annidati sotto di esso.

Un oggetto flusso è analogo alla nozione tradizionale di un file. Analogamente a un file, un flusso contiene dati archiviati come sequenza consecutiva di byte.

Un file composto COM è costituito da un oggetto di archiviazione radice che contiene almeno un oggetto flusso che rappresenta i dati nativi insieme a uno o più oggetti di archiviazione corrispondenti agli oggetti collegati e incorporati. L'oggetto di archiviazione radice viene mappato a un nome di file in qualsiasi file system risieda. Tutti gli oggetti all'interno del documento sono rappresentati anche da un oggetto di archiviazione contenente uno o più oggetti flusso e probabilmente che contengono anche uno o più oggetti di archiviazione. In questo modo, un documento può essere costituito da un numero illimitato di oggetti annidati. Per ulteriori informazioni, vedere [file composti](compound-files.md).

 

 




