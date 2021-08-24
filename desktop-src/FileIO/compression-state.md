---
description: Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno stato di compressione.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Stato di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19abfe0deecb951c00dacb00c64dd8dcf7af56d37fe9112095cdce403619f843
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582421"
---
# <a name="compression-state"></a>Stato di compressione

Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno *stato di compressione*.

Mentre l'attributo di compressione di un file o di una directory indica semplicemente se il file o la directory è compressa o meno, lo stato di compressione specifica anche il formato dei dati compressi.

Usare il [**codice di controllo \_ FSCTL GET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) per determinare lo stato di compressione di un file o di una directory.

Lo stato di compressione viene codificato come valore a 16 bit. Un valore dello stato di compressione COMPRESSION \_ FORMAT \_ NONE indica che un file non è compresso. Il valore COMPRESSION \_ FORMAT DEFAULT indica che un file è compresso, utilizzando il formato di compressione \_ predefinito. Qualsiasi altro valore indica che un file è compresso, utilizzando il formato di compressione specificato dal valore dello stato di compressione.

Usare il [**codice di controllo \_ FSCTL SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) per impostare lo stato di compressione di un file o di una directory. Questa operazione imposta anche l'attributo di compressione del file o della directory.

L'impostazione dello stato di compressione di un file su un valore diverso da zero comprime il file usando il formato di compressione codificato dal valore dello stato di compressione. Se si imposta lo stato di compressione di un file su zero, il file viene decompresso. Si tratta di operazioni sincrone. Il file viene compresso o decompresso immediatamente quando si imposta lo stato di compressione.

L'impostazione dello stato di compressione di una directory non causa alcuna compressione o decompressione immediata. Al contrario, l'impostazione dello stato di compressione di una directory imposta uno stato di compressione predefinito che verrà assegnato a tutti i file e le sottodirectory appena creati.

 

 
