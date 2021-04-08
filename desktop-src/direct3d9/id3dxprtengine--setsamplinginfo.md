---
description: Imposta le proprietà di campionamento utilizzate dal simulatore di trasferimento di luminosità (PRT) pre-calcolato.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'Metodo ID3DXPRTEngine:: SetSamplingInfo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ab229652fe9e333519acce7d8474d3c4f0cf7ef9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762125"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>Metodo ID3DXPRTEngine:: SetSamplingInfo

Imposta le proprietà di campionamento utilizzate dal simulatore di trasferimento di luminosità (PRT) pre-calcolato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NumRays* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Numero di raggi luminosi da indirizzare a ogni campione. Deve essere maggiore di zero.

</dd> <dt>

*UseSphere* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, gli esempi verranno calcolati su una sfera completa. Se **false**, gli esempi verranno calcolati su un emisfero.

</dd> <dt>

*UseCosine* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **true**, usare una ponderazione del coseno degli esempi. Se UseCosine e UseSphere sono **true**, il metodo avrà esito negativo e verrà restituito un errore.

</dd> <dt>

*Adattivo* \[ in\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Deve essere **false**. Il campionamento adattivo non è attualmente implementato.

</dd> <dt>

*AdaptiveThresh* \[ in\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, e \_ NOTIMPL, e \_ OutOfMemory.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
