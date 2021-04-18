---
title: Funzione D3DX12GetBaseSubobjectType (D3dx12. h)
description: Restituisce il tipo di sottooggetto che corrisponde alla classe di base del tipo di sottooggetto passato.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType (funzione)
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322176"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>D3DX12GetBaseSubobjectType (funzione)

Restituisce il tipo di sottooggetto che corrisponde alla classe di base del tipo di sottooggetto passato.

## <a name="syntax"></a>Sintassi


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sottoobjecttype* 
</dt> <dd>

Tipo: **\_ \_ \_ \_ tipo di sottooggetto stato della pipeline D3D12**

Valore di enumerazione che specifica il tipo di sottooggetto a cui si è interessati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **\_ \_ \_ \_ tipo di sottooggetto stato della pipeline D3D12**

Se *subobjecttype* corrisponde a un tipo di dati SubObject derivato da un altro tipo di dati SubObject, viene restituito il tipo di oggetto SubObject del tipo di dati SubObject di base. in caso contrario, viene restituito il tipo di sottooggetto passato. Se, ad esempio, viene passato il STENCIL1 di profondità del **\_ \_ \_ \_ tipo \_ \_ di sottooggetto stato della pipeline D3D12** , viene restituito **\_ \_ lo \_ stencil di profondità del \_ tipo \_ \_ di sottooggetto stato** della pipeline D3D12.

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





