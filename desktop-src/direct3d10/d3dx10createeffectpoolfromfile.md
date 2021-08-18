---
description: Creare un pool di effetti da un file degli effetti.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Funzione D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 500e0a72bc239b6c3f67011ed7abc0421f11cd8b9e4f67cbc86087e45027522d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753401"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a>Funzione D3DX10CreateEffectPoolFromFile

Creare un pool di effetti da un file degli effetti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Nome file dell'effetto. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati viene risolto in LPCSTR.

</dd> <dt>

*pDefines* \[ Pollici\]
</dt> <dd>

Tipo: **const [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***

Matrice con terminazione NULL di macro shader (vedere [**D3D \_ SHADER \_ MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare questa proprietà su **NULL** per non specificare macro.

</dd> <dt>

*pInclude* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***

Puntatore a un'interfaccia di inclusione (vedere [**ID3D10Include Interface).**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) Questo parametro può essere **NULL**.

</dd> <dt>

*pProfile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Stringa che specifica il profilo [shader](../direct3dhlsl/dx-graphics-hlsl-models.md)o il modello di shader.

</dd> <dt>

*HLSLFlags* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opzioni di compilazione HLSL (vedere [Costanti SHADER \_ D3D10).](d3d10-shader.md)

</dd> <dt>

*FXFlags* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Opzioni di compilazione degli effetti (vedere [Flag di compilazione e flag di effetto).](d3d10-graphics-reference-effect-constants.md)

</dd> <dt>

*pDevice* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***

Puntatore al dispositivo (vedere [**ID3D10 InterfaceDevice Interface)**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)che userà le risorse.

</dd> <dt>

*pPump* \[ Pollici\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***

Puntatore a un'interfaccia pump di thread (vedere [**l'interfaccia ID3DX10ThreadPump).**](id3dx10threadpump.md) Usare **NULL** per specificare che questa funzione non deve restituire alcun valore finché non viene completata.

</dd> <dt>

*ppEffectPool* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***

Indirizzo di un puntatore al pool di effetti (vedere [**l'interfaccia ID3D10EffectPool).**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)

</dd> <dt>

*ppErrors* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Indirizzo di un puntatore alla memoria (vedere [**l'interfaccia ID3D10Blob)**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)che contiene gli eventuali errori di compilazione dell'effetto.

</dd> <dt>

*pHResult* \[ Cambio\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntatore al valore restituito. Può essere **NULL.** Se *pPump* non è **NULL,** *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questo esempio crea un pool di effetti dall'effetto usato nell'esempio [BasicHLSL10.](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3DX10Async.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
