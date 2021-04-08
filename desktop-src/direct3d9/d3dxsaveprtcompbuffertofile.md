---
description: Salva nel disco un buffer di trasferimento di luminosità precalcolata (PRT) compresso.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Funzione D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
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
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969344"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>D3DXSavePRTCompBufferToFile (funzione)

Salva nel disco un buffer di trasferimento di luminosità precalcolata (PRT) compresso.

## <a name="syntax"></a>Sintassi

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Parametri

*pFileName* \[ in\]

Tipo: **[LPCSTR](../winprog/windows-data-types.md)**

Nome del file in cui deve essere salvato il buffer compresso.

*pbuffer* \[ in\]

Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Indirizzo di un puntatore all'oggetto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) di input.

## <a name="return-value"></a>Valore restituito

Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**

Se il metodo ha esito positivo, il valore restituito è **D3D \_ OK**. Se il metodo ha esito negativo, il valore restituito può essere **D3DERR \_ INVALIDCALL**.

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

Per i casi in cui *bIsTex* è diverso da zero, *NumSamples valore* deve essere uguale a `TexWidth * TexHeight` .

Il blocco di dati di base che segue l'intestazione è `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` byte.

Di seguito è riportato il blocco di dati di APC weights, che è `NumPCA * NumSamples * sizeof(float)` byte.

Se *NumClusters* è maggiore di 1, il file termina con il blocco di dati degli ID cluster di `NumSamples * sizeof(UINT)` byte.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Vedi anche

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
