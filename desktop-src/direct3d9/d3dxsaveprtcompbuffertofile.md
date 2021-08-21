---
description: Salva un buffer PRT (Precomputed Radiance Transfer) compresso su disco.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Funzione D3DXSavePRTCompBufferToFile (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a62bd164ce8eb8175c62658b19dd5ce6282d6c75b081db45f8b0af4994322579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524511"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>Funzione D3DXSavePRTCompBufferToFile

Salva un buffer PRT (Precomputed Radiance Transfer) compresso su disco.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parametri

*pFileName* \[ Pollici\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome del file in cui deve essere salvato il buffer compresso.

*pBuffer* \[ Pollici\]

Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Indirizzo di un puntatore [**all'oggetto ID3DXPRTCompBuffer di**](id3dxprtcompbuffer.md) input.

## <a name="return-value"></a>Valore restituito

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se il metodo ha esito positivo, il valore restituito è **D3D \_ OK.** Se il metodo ha esito negativo, il valore restituito può **essere D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in [D3DXSavePRTCompBufferToFileW](). In caso contrario, la chiamata di funzione viene risolta in **D3DXSavePRTCompBufferToFileA**.

Il formato di file PCA è un file binario sotto forma di intestazione e quindi di due o tre blocchi di dati.

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

Se *bIsTex* è diverso da zero, *NumSamples* deve essere uguale a `TexWidth * TexHeight` .

Il blocco di dati di base che segue l'intestazione è `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` byte.

Di seguito è riportato il blocco di dati weights PCA, ovvero `NumPCA * NumSamples * sizeof(float)` byte.

Se *NumClusters* è maggiore di 1, il file termina con il blocco di dati degli ID cluster di `NumSamples * sizeof(UINT)` byte.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |

## <a name="see-also"></a>Vedi anche

[Funzioni di trasferimento di radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
