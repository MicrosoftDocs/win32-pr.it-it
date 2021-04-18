---
description: L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilizzi e valori letterali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304357"
---
# <a name="usages-and-literals-direct3d-9"></a>Utilizzi e valori letterali (Direct3D 9)

L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore  | Descrizione                                                                                                                                                                                                                                                                         |
| const  | Il parametro sarà costante nell'ambito di tutte le funzioni. Si noti che tali parametri possono comunque essere scritti con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), perché questo errore si verifica al di fuori dell'ambito di tutte le funzioni. |
| shared | Il parametro verrà condiviso nel pool di effetti.                                                                                                                                                                                                                                    |
| static | Il parametro sarà invisibile per l'applicazione, ovvero non è possibile accedervi da [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).                                                                                                  |



 

Contrassegnando un parametro come valore letterale viene indicato che il valore non viene mai modificato. Ciò consente al compilatore degli effetti di eseguire un'ottimizzazione aggiuntiva.

Solo i parametri di primo livello non condivisi possono essere contrassegnati come valori letterali. I parametri possono essere contrassegnati solo come valori letterali con [**ID3DXEffectCompiler**](id3dxeffectcompiler.md). Non è possibile impostare valori letterali con [**ID3DXEffect**](id3dxeffect.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



