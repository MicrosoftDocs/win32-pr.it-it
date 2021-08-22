---
title: D3DCOMPILE_EFFECT costanti (D3DCompiler.h)
description: Queste costanti indirizzano il modo in cui il compilatore compila un file degli effetti o come il runtime elabora il file dell'effetto.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d5c31efb17d2f852ac3903a5946ce5fb72fcef86ef083c474328859472c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118286915"
---
# <a name="d3dcompile_effect-constants"></a>Costanti D3DCOMPILE \_ EFFECT

Queste costanti indirizzano il modo in cui il compilatore compila un file degli effetti o come il runtime elabora il file dell'effetto.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**EFFETTO FIGLIO DELL'EFFETTO D3DCOMPILE \_ \_ \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compilare il file degli effetti (con estensione fx) in un effetto figlio. Gli effetti figlio non hanno inizializzatori per i valori condivisi perché questi effetti figlio vengono inizializzati nell'effetto master (pool di effetti).

> [!Note]  
> I pool di effetti sono supportati da Effects 10 (FX10), ma non da Effects 11 (FX11). Per altre informazioni sulle differenze tra i pool di effetti in Direct3D 10 e i gruppi di effetti in Direct3D 11, vedere [Pool di effetti e gruppi](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**L'EFFETTO D3DCOMPILE \_ \_ CONSENTE OPERAZIONI \_ \_ LENTE**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Disabilita la modalità prestazioni e consente oggetti di stato modificabili.

Per impostazione predefinita, la modalità prestazioni è abilitata. La modalità prestazioni non consente la visualizzazione di oggetti di stato modificabili impedendo la visualizzazione di espressioni non letterali nelle definizioni degli oggetti di stato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DCompiler.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

