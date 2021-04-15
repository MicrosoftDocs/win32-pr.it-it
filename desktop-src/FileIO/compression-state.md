---
description: Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno stato di compressione.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Stato di compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231755"
---
# <a name="compression-state"></a>Stato di compressione

Ogni file e directory in un volume che supporta la compressione per singoli file e directory ha uno *stato di compressione*.

Mentre l'attributo di compressione di un file o di una directory indica semplicemente se il file o la directory è compresso o non compresso, lo stato di compressione specifica anche il formato di tutti i dati compressi.

Usare il codice di controllo della [**\_ \_ compressione FSCTL Get**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) per determinare lo stato di compressione di un file o di una directory.

Lo stato di compressione è codificato come valore a 16 bit. Un valore dello stato di compressione del formato di compressione \_ \_ None indica che un file non è compresso. Il valore predefinito per il formato di compressione \_ \_ indica che un file è compresso, usando il formato di compressione predefinito. Qualsiasi altro valore indica che un file è compresso, usando il formato di compressione specificato dal valore dello stato di compressione.

Usare il codice di controllo della [**\_ \_ compressione FSCTL set**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) per impostare lo stato di compressione di un file o di una directory. Questa operazione imposta anche l'attributo di compressione del file o della directory.

L'impostazione dello stato di compressione di un file su un valore diverso da zero comprime il file, usando il formato di compressione codificato dal valore dello stato di compressione. Impostando lo stato di compressione di un file su zero, il file viene decompresso. Si tratta di operazioni sincrone. Il file viene compresso o decompresso immediatamente quando si imposta lo stato di compressione.

L'impostazione dello stato di compressione di una directory non provoca alcuna compressione o decompressione immediata. Se invece si imposta lo stato di compressione di una directory, viene impostato uno stato di compressione predefinito che verrà assegnato a tutti i file e le sottodirectory appena creati.

 

 
