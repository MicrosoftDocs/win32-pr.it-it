---
description: Definisce una matrice di quantizzazione.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: Struttura DXVA_Qmatrix_HEVC (DXVA. h)
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
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524546"
---
# <a name="dxva_qmatrix_hevc-structure"></a>\_Struttura DXVA Qmatrix \_ HEVC

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

Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 4x4, corrispondente a \[ \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, inclusivo e i è compreso tra 0 e 15 inclusi.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 8x8 Virtual, corrispondente a scalar \[ 1 \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, incluso e i è compreso tra 0 e 63, inclusi.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 8x8 Virtual, corrispondente a scalar \[ 2 \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo da 0 a 5, incluso e i è compreso tra 0 e 63, inclusi.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contiene gli elenchi di ridimensionamento per il processo di ridimensionamento 8x8 Virtual, corrispondenti a scaling \[ 3 \] \[ MatrixID \] \[ i \] nella specifica HEVC, dove MatrixID è compreso nell'intervallo tra 0 e 1, inclusivo e i è compreso tra 0 e 63, inclusi.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contiene il valore del controller di dominio dell'elenco di ridimensionamento per le dimensioni 16x16 con sizeID uguale a 2 e corrispondente all'elenco di ridimensionamento \_ \_ DC \_ coefficiente \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID uguale a 2 e matrixID nell'intervallo compreso tra 0 e 5, incluso, nella specifica HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contiene il valore del controller di dominio dell'elenco di ridimensionamento per le dimensioni di 32x32 con sizeID uguale a 3 e corrispondente all'elenco di ridimensionamento \_ \_ DC \_ coefficiente \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID uguale a 3 e matrixID nell'intervallo compreso tra 0 e 1, inclusi, nella specifica HEVC.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




