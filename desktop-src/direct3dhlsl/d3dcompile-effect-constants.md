---
title: Costanti D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Queste costanti indirizzano il modo in cui il compilatore compila un file di effetti o il modo in cui il runtime elabora il file di effetti.
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
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982121"
---
# <a name="d3dcompile_effect-constants"></a>\_Costanti effetto D3DCOMPILE

Queste costanti indirizzano il modo in cui il compilatore compila un file di effetti o il modo in cui il runtime elabora il file di effetti.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_Effetto D3DCOMPILE effetto \_ figlio \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compilare il file Effects (. FX) in un effetto figlio. Gli effetti figlio non hanno inizializzatori per i valori condivisi, perché questi effetti figlio vengono inizializzati nell'effetto principale (il pool di effetti).

> [!Note]  
> I pool di effetti sono supportati dagli effetti 10 (FX10) ma non dagli effetti 11 (FX11). Per altre informazioni sulle differenze tra i pool di effetti in Direct3D 10 e sui gruppi di effetti in Direct3D 11, vedere [pool di effetti e gruppi](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE \_ Effect \_ consente \_ \_ operazioni lente**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Disabilita la modalità di prestazioni e consente oggetti di stato modificabili.

Per impostazione predefinita, è abilitata la modalità prestazioni. La modalità prestazioni non consente oggetti di stato modificabili impedendo la visualizzazione di espressioni non letterali nelle definizioni degli oggetti di stato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

