---
description: Creare un token del numero di versione di vertex shader.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 861295c9068bee9e40174d877a78628aa405b9cfa5d46414190fbb7b37904e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527257"
---
# <a name="d3dvs_version-macro"></a>Macro D3DVS \_ VERSION

Creare un token del numero di versione di vertex shader.

## <a name="syntax"></a>Sintassi


```C++
DWORD D3DVS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*\_Principali* 
</dt> <dd>

Versione principale del vertex shader. Vedere le osservazioni per i valori appropriati.

</dd> <dt>

*\_Minorenne* 
</dt> <dd>

Versione del vertex shader secondario. Vedere le osservazioni per i valori appropriati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore DWORD che è una versione vertex shader.

## <a name="remarks"></a>Commenti

Numeri di versione

Il numero di versione è una combinazione della versione principale e dei numeri di versione del vertex shader secondario. I numeri validi vengono visualizzati nella tabella.



| Principale | Minorenne | Esempio             |
|-------|-------|---------------------|
| 1     | 1     | VERSIONE \_ D3DVS(1,1) |
| 2     | 0     | VERSIONE \_ D3DVS(2,0) |
| 3     | 0     | VERSIONE \_ D3DVS(3,0) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




