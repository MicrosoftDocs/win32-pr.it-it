---
description: Salva un buffer PRT (Precomputed Radiance Transfer) su disco.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Funzione D3DXSavePRTBufferToFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfa3d06970d138ff1c868403c20bb41cf14f0a5cbb7116cbe0f0843a51258dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524531"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>Funzione D3DXSavePRTBufferToFile

Salva un buffer PRT (Precomputed Radiance Transfer) su disco.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parametri

*pFileName* \[ Pollici\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome del file in cui deve essere salvato il buffer.

*pBuffer* \[ Pollici\]

Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Indirizzo di un puntatore [**all'oggetto ID3DXPRTBuffer di**](id3dxprtbuffer.md) input.

## <a name="return-value"></a>Valore restituito

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se il metodo ha esito positivo, il valore restituito è **D3D \_ OK.** Se il metodo ha esito negativo, il valore restituito può **essere D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se unicode è definito, la chiamata di funzione viene risolta in [D3DXSavePRTBufferToFileW](). In caso contrario, la chiamata di funzione viene risolta in **D3DXSavePRTBufferToFileA**.

Il formato di file PRT è un file binario sotto forma di intestazione e quindi di blocco di dati.

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

Se *bIsTex* è diverso da zero, *NumSamples* deve essere uguale a `TexWidth * TexHeight` .

Il blocco di dati che segue l'intestazione è `NumSamples * NumCoeffs * NumChannels * sizeof(float)` byte.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Vedi anche

[Funzioni di trasferimento della radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
