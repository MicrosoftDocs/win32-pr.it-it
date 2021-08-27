---
description: Rimuovere un osso.
ms.assetid: efb88108-5c76-47c8-b8ce-1ba29cb18ba4
title: Metodo ID3DX10SkinInfo::RemoveBone (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemoveBone
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f26a19c0903056c6de62ae72852b19557b0926fe5b2616adfa8d77bd945cba4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119941"
---
# <a name="id3dx10skininforemovebone-method"></a>Metodo ID3DX10SkinInfo::RemoveBone

Rimuovere un osso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveBone(
  [in] UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Indice che specifica quale osso rimuovere. Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
