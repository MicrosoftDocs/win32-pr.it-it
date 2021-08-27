---
description: L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilizzi e valori letterali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b8c9fa8eb30726e783ce763ec8700f715dbd5d2b85ff3bf98340cf604e8e2f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026011"
---
# <a name="usages-and-literals-direct3d-9"></a>Utilizzi e valori letterali (Direct3D 9)

L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.



| Valore  | Descrizione                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| const  | Il parametro sarà costante nell'ambito di tutte le funzioni. Si noti che tali parametri possono comunque essere scritti in con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), perché ciò si verifica all'esterno dell'ambito di tutte le funzioni. |
| shared | Il parametro verrà condiviso nel pool di effetti.                                                                                                                                                                                                                                    |
| static | Il parametro non sarà visibile all'applicazione, in altri modo non sarà possibile accedervi da [**ID3DXEffect**](id3dxeffect.md) [**o ID3DXEffectCompiler.**](id3dxeffectcompiler.md)                                                                                                  |



 

Se si contrassegna un parametro come valore letterale, il relativo valore non cambierà mai. Ciò consente al compilatore di effetti di eseguire un'ottimizzazione aggiuntiva.

Solo i parametri di primo livello non condivisi possono essere contrassegnati come valori letterali. I parametri possono essere contrassegnati come letterali solo [**con ID3DXEffectCompiler**](id3dxeffectcompiler.md). I valori letterali non possono essere impostati [**con ID3DXEffect.**](id3dxeffect.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



