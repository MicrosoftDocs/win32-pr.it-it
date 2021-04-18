---
description: Definisce le dimensioni della finestra di una superficie di destinazione di rendering su cui si proietta un volume 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Struttura D3DVIEWPORT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVIEWPORT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3d96000de50934ebdc893ffc3866dd3252703bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323026"
---
# <a name="d3dviewport9-structure"></a>Struttura D3DVIEWPORT9

Definisce le dimensioni della finestra di una superficie di destinazione di rendering su cui si proietta un volume 3D.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DVIEWPORT9 {
  DWORD X;
  DWORD Y;
  DWORD Width;
  DWORD Height;
  float MinZ;
  float MaxZ;
} D3DVIEWPORT9, *LPD3DVIEWPORT9;
```



## <a name="members"></a>Members

<dl> <dt>

**X**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata pixel dell'angolo superiore sinistro del viewport sulla superficie di destinazione di rendering. A meno che non si desideri eseguire il rendering in un subset della superficie, questo membro può essere impostato su 0.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata pixel dell'angolo superiore sinistro del viewport sulla superficie di destinazione di rendering. A meno che non si desideri eseguire il rendering in un subset della superficie, questo membro può essere impostato su 0.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione della larghezza del volume di ritaglio, in pixel. A meno che non si esegua il rendering solo in un subset della superficie, questo membro deve essere impostato sulla dimensione Width della superficie di destinazione di rendering.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione dell'altezza del volume di ritaglio, in pixel. A meno che non si esegua il rendering solo in un subset della superficie, questo membro deve essere impostato sulla dimensione Height della superficie di destinazione di rendering.

</dd> <dt>

**MinZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Insieme a MaxZ, valore che descrive l'intervallo di valori di profondità in cui deve essere eseguito il rendering di una scena, i valori minimo e massimo del volume di ritaglio. La maggior parte delle applicazioni imposta questo valore su 0,0. Il ritaglio viene eseguito dopo l'applicazione della matrice di proiezione.

</dd> <dt>

**MaxZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Insieme a MinZ, valore che descrive l'intervallo di valori di profondità in cui deve essere eseguito il rendering di una scena, i valori minimo e massimo del volume di ritaglio. La maggior parte delle applicazioni imposta questo valore su 1,0. Il ritaglio viene eseguito dopo l'applicazione della matrice di proiezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri X, Y, larghezza e altezza descrivono la posizione e le dimensioni del viewport sulla superficie di destinazione di rendering. In genere, le applicazioni eseguono il rendering sull'intera superficie di destinazione; Quando si esegue il rendering in una superficie 640 x 480, i membri devono essere rispettivamente 0, 0, 640 e 480. MinZ e MaxZ vengono in genere impostati su 0,0 e 1,0, ma possono essere impostati su altri valori per ottenere effetti specifici. Ad esempio, è possibile impostare entrambi su 0,0 per forzare il rendering degli oggetti in primo piano di una scena o entrambi a 1,0 per forzare gli oggetti in background.

Quando i parametri del viewport per un dispositivo cambiano (a causa di una chiamata al metodo [**seviewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) ), il driver compila una nuova matrice di trasformazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**Viewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
