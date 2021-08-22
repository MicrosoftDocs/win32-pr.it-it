---
description: Definisce una matrice di quantizzazione.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC struttura (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 5d71b392d41c123eb0106d08f1a75d2a5147977b106c811e0bf0786ab2acff2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974590"
---
# <a name="dxva_qmatrix_hevc-structure"></a>Struttura DXVA \_ Qmatrix \_ HEVC

Definisce una matrice di quantizzazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a>Members

<dl> <dt>

**ucScalingLists0 \[ 6 \] \[ 16\]**
</dt> <dd>

Contiene gli elenchi di scalabilità per il processo di ridimensionamento 4x4, corrispondenti a ScalingList 0 MatrixID i nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, inclusi e i è compreso nell'intervallo compreso tra 0 e \[ \] \[ \] \[ \] 15 inclusi.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene gli elenchi di scalabilità per il processo di ridimensionamento 8x8, corrispondenti a ScalingList 1 MatrixID i nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, inclusi e i è compreso nell'intervallo compreso tra 0 e \[ \] \[ \] \[ \] 63, inclusi.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene gli elenchi di scalabilità per il processo di ridimensionamento 8x8, corrispondenti a ScalingList 2 MatrixID i nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, inclusi e i è compreso nell'intervallo compreso tra 0 e \[ \] \[ \] \[ \] 63 inclusi.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contiene gli elenchi di scalabilità per il processo di ridimensionamento 8x8, corrispondenti a ScalingList 3 MatrixID i nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 1, inclusi e i è compreso nell'intervallo compreso tra 0 e \[ \] \[ \] \[ \] 63, inclusi.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contiene il valore DC dell'elenco di scalabilità per dimensioni 16x16 con sizeID uguale a 2 e corrispondente all'elenco di scala \_ \_ dc \_ coef \_ minus8 \[ sizeID • 2 matrixID +8 con sizeID uguale a 2 e matrixID nell'intervallo compreso tra 0 e \] \[ \] 5, inclusi, nella specifica HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contiene il valore DC dell'elenco di scalabilità per dimensioni 32x32 con sizeID uguale a 3 e corrispondente all'elenco di scala \_ \_ dc \_ coef \_ minus8 \[ sizeID - 2 matrixID +8 con sizeID uguale a 3 e matrixID nell'intervallo compreso tra 0 e \] \[ \] 1, inclusi, nella specifica HEVC.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation strutture](media-foundation-structures.md)
</dt> </dl>

 

 




