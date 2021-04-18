---
description: Salva nel disco un buffer di trasferimento di luminosità (PRT) pre-calcolato.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Funzione D3DXSavePRTBufferToFile (D3DX9Mesh. h)
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
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322602"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>D3DXSavePRTBufferToFile (funzione)

Salva nel disco un buffer di trasferimento di luminosità (PRT) pre-calcolato.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Parametri

*pFileName* \[ in\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome del file in cui salvare il buffer.

*pbuffer* \[ in\]

Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input.

## <a name="return-value"></a>Valore restituito

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se il metodo ha esito positivo, il valore restituito è **D3D \_ OK**. Se il metodo ha esito negativo, il valore restituito può essere **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in [D3DXSavePRTBufferToFileW](). In caso contrario, la chiamata di funzione viene risolta in **D3DXSavePRTBufferToFileA**.

Il formato del file PRT è costituito da un file binario sotto forma di intestazione e quindi da un blocco di dati.

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

Per i casi in cui *bIsTex* è diverso da zero, *NumSamples valore* deve essere uguale a `TexWidth * TexHeight` .

Il blocco di dati che segue l'intestazione è `NumSamples * NumCoeffs * NumChannels * sizeof(float)` byte.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Vedi anche

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
