---
description: La convalida viene eseguita durante la compilazione dell'effetto. Per convalidare la tecnica corrente, specificare NULL come handle della tecnica da convalidare.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Convalida (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d6c49f3bdf3bc0ba75f52bd8138fa6f5d777c3613d105b2706929c01b3ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519440"
---
# <a name="validation-direct3d-9"></a>Convalida (Direct3D 9)

La convalida viene eseguita durante la compilazione dell'effetto. Per convalidare la tecnica corrente, specificare **NULL** come handle della tecnica da convalidare.

La convalida avrà esito negativo per uno degli elementi seguenti:

-   Se l'handle della tecnica specificato non esiste.
-   Se l'applicazione di uno stato in qualsiasi passaggio della tecnica ha esito negativo.
-   Se la convalida del dispositivo non riesce dopo l'applicazione di tutti gli stati in qualsiasi passaggio della tecnica.
-   Se agli stati dell'effetto PIXELSHADER o VERTEXSHADER vengono assegnati shader non validi in qualsiasi passaggio della tecnica.
-   Se le estremità del dispositivo non supportano il mapping del cubo e a uno stato dell'effetto TEXTURE viene assegnato un valore di tipo textureCUBE in qualsiasi passaggio della tecnica.
-   Se le estremità del dispositivo non supportano il mapping del volume e a uno stato dell'effetto TEXTURE viene assegnato un valore di tipo texture3D in qualsiasi passaggio della tecnica.

Per altre informazioni, vedere [Stati degli effetti (Direct3D 9).](effect-states.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



