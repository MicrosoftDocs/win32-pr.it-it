---
description: La convalida viene eseguita durante la compilazione dell'effetto. Per convalidare la tecnica corrente, specificare NULL come handle della tecnica da convalidare.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Convalida (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303916"
---
# <a name="validation-direct3d-9"></a>Convalida (Direct3D 9)

La convalida viene eseguita durante la compilazione dell'effetto. Per convalidare la tecnica corrente, specificare **null** come handle della tecnica da convalidare.

La convalida avrà esito negativo per uno dei seguenti elementi:

-   Se l'handle di tecnica specificato non esiste.
-   Se l'applicazione di qualsiasi stato in qualsiasi passaggio della tecnica ha esito negativo.
-   Se la convalida del dispositivo ha esito negativo dopo l'applicazione di tutti gli stati in qualsiasi passaggio della tecnica.
-   Se agli Stati dell'effetto PIXELSHADER o VERTEXSHADER vengono assegnati shader non validi in qualsiasi passaggio della tecnica.
-   Se i tappi dei dispositivi non supportano il mapping dei cubi e a uno stato di effetto trama viene assegnato un valore di tipo textureCUBE in qualsiasi passaggio della tecnica.
-   Se i tappi dei dispositivi non supportano il mapping del volume e a uno stato di effetto trama viene assegnato un valore di tipo texture3D in qualsiasi passaggio della tecnica.

Per altre informazioni, vedere [Stati degli effetti (Direct3D 9)](effect-states.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



