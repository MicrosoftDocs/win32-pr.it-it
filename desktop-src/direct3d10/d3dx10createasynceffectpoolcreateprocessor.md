---
description: Creare un processore di dati asincrono per un pool di memoria.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: Funzione D3DX10CreateAsyncEffectPoolCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235076"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a>D3DX10CreateAsyncEffectPoolCreateProcessor (funzione)

Creare un processore di dati asincrono per un pool di memoria.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che contiene il nome file dell'effetto.

</dd> <dt>

*pDefines* \[ in\]
</dt> <dd>

Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.

</dd> <dt>

*pInclude* \[ in\]
</dt> <dd>

Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**

Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.

</dd> <dt>

*pProfile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md) o il modello dello shader.

</dd> <dt>

*Flag* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opzioni di compilazione HLSL (vedere [flag shader](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*FXFlags* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Opzioni di compilazione degli effetti (vedere [flag di compilazione ed effetto](d3d10-graphics-reference-effect-constants.md)).

</dd> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.

</dd> <dt>

*ppErrorBuffer* \[ out\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.

</dd> <dt>

*ppDataProcessor* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***

Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
