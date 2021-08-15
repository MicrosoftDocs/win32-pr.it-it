---
description: Definisce le dimensioni della finestra di una superficie di destinazione di rendering su cui proietta un volume 3D.
ms.assetid: fb2c6048-f837-497d-8e4f-e18942d37899
title: Struttura D3DVIEWPORT9 (D3D9Types.h)
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
ms.openlocfilehash: 40162e4350e5a68670023701f1cdae973fb8a7bac3a6d4f5c301136c4e8c2702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527267"
---
# <a name="d3dviewport9-structure"></a>Struttura D3DVIEWPORT9

Definisce le dimensioni della finestra di una superficie di destinazione di rendering su cui proietta un volume 3D.

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

Coordinata in pixel dell'angolo superiore sinistro del viewport sulla superficie di destinazione di rendering. A meno che non si voglia eseguire il rendering in un subset della superficie, questo membro può essere impostato su 0.

</dd> <dt>

**S**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Coordinata in pixel dell'angolo superiore sinistro del viewport sulla superficie di destinazione di rendering. A meno che non si voglia eseguire il rendering in un subset della superficie, questo membro può essere impostato su 0.

</dd> <dt>

**Larghezza**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione larghezza del volume della clip, in pixel. A meno che il rendering non venga eseguito solo in un subset della superficie, questo membro deve essere impostato sulla dimensione larghezza della superficie di destinazione del rendering.

</dd> <dt>

**Altezza**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dimensione dell'altezza del volume della clip, in pixel. A meno che il rendering non venga eseguito solo su un subset della superficie, questo membro deve essere impostato sulla dimensione altezza della superficie di destinazione del rendering.

</dd> <dt>

**MinZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Insieme a MaxZ, valore che descrive l'intervallo di valori di profondità in cui eseguire il rendering di una scena, i valori minimo e massimo del volume della clip. La maggior parte delle applicazioni imposta questo valore su 0,0. Il ritaglio viene eseguito dopo l'applicazione della matrice di proiezione.

</dd> <dt>

**MaxZ**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Insieme a MinZ, valore che descrive l'intervallo di valori di profondità in cui eseguire il rendering di una scena, i valori minimo e massimo del volume della clip. La maggior parte delle applicazioni imposta questo valore su 1.0. Il ritaglio viene eseguito dopo l'applicazione della matrice di proiezione.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri X, Y, Width e Height descrivono la posizione e le dimensioni del viewport sulla superficie di destinazione di rendering. In genere, il rendering delle applicazioni viene eseguito sull'intera superficie di destinazione. Quando si esegue il rendering su una superficie 640 x 480, questi membri devono essere rispettivamente 0, 0, 640 e 480. MinZ e MaxZ sono in genere impostati su 0.0 e 1.0, ma possono essere impostati su altri valori per ottenere effetti specifici. Ad esempio, è possibile impostarli entrambi su 0.0 per forzare il sistema a eseguire il rendering degli oggetti in primo piano di una scena o entrambi su 1.0 per forzare gli oggetti in background.

Quando i parametri del viewport per un dispositivo cambiano (a causa di una chiamata al [**metodo SetViewport),**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) il driver compila una nuova matrice di trasformazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
</dt> <dt>

[**SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)
</dt> </dl>

 

 
