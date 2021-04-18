---
description: Creare un token di numero di versione del vertex shader.
ms.assetid: c3aa6b01-7949-4171-a8b5-2f453fd7a422
title: D3DVS_VERSION macro (D3d9types. h)
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
ms.openlocfilehash: 915d5b843287602c80572d739d8b369d8c301770
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323021"
---
# <a name="d3dvs_version-macro"></a>D3DVS \_ versione macro

Creare un token di numero di versione del vertex shader.

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

Versione principale del vertex shader. Vedere la sezione Osservazioni per i valori appropriati.

</dd> <dt>

*\_Minorenne* 
</dt> <dd>

Versione del vertex shader secondaria. Vedere la sezione Osservazioni per i valori appropriati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore DWORD che è una versione del vertex shader.

## <a name="remarks"></a>Commenti

Numeri di versione

Il numero di versione è una combinazione della versione principale e dei numeri di versione di vertex shader secondari. I numeri validi sono visualizzati nella tabella.



| Principale | Minorenne | Esempio             |
|-------|-------|---------------------|
| 1     | 1     | \_Versione di D3DVS (1,1) |
| 2     | 0     | \_Versione di D3DVS (2, 0) |
| 3     | 0     | \_Versione di D3DVS (3, 0) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Macro](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




