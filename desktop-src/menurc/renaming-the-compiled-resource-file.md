---
title: Ridenominazione del file di risorse compilato
description: Per impostazione predefinita, quando si compilano risorse, RC denomina il file di risorse compilato (res) con il nome di base del file RC e lo inserisce nella stessa directory del file RC.
ms.assetid: be120032-666f-4627-8f98-96bde7c55fa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c54e22cff753dbc59cbce61cd71874c8fe77a85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220985"
---
# <a name="renaming-the-compiled-resource-file"></a>Ridenominazione del file di risorse compilato

Per impostazione predefinita, quando si compilano risorse, RC denomina il file di risorse compilato (res) con il nome di base del file RC e lo inserisce nella stessa directory del file RC. CVTRES deve quindi essere richiamato per convertire il file con estensione RES in un formato di risorsa binario (con estensione RBJ) che può essere riconosciuto dal linker. Nell'esempio seguente viene compilato MyApp. RC e viene creato un file di risorse compilato denominato MyApp. res nella stessa directory di MyApp. RC:

**RC MyApp. RC**

L'opzione **/fo** assegna al file res risultante un nome diverso dal nome del file RC corrispondente. Ad esempio, per assegnare un nome al file res. res risultante, usare il comando seguente:

**RC-fo NewFile. res MyApp. RC**

L'opzione **/fo** può anche inserire il file con estensione RES in una directory diversa. Il comando seguente, ad esempio, inserisce il file di risorse compilato MyApp. res nella directory C: \\ source \\ Resource:

**RC-fo c: \\ risorsa di origine \\ \\ MyApp. res MyApp. RC**

 

 




