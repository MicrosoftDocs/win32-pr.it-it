---
description: Crea una trama da un file.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Funzione D3DXCreateTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401963"
---
# <a name="d3dxcreatetexturefromfile-function"></a>D3DXCreateTextureFromFile (funzione)

Crea una trama da un file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama.

</dd> <dt>

*pSrcFile* \[ in\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntatore a una stringa che specifica il nome del file. Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR. In caso contrario, il tipo di dati String viene risolto in LPCSTR. Vedere la sezione Osservazioni.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta l'oggetto trama creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.

## <a name="remarks"></a>Commenti

L'impostazione del compilatore determina anche la versione della funzione. Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileW. In caso contrario, la chiamata di funzione viene risolta in D3DXCreateTextureFromFileA perché vengono utilizzate le stringhe ANSI.

Questa funzione supporta i formati di file seguenti:. bmp,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm e. tga. Vedere [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).

La funzione è equivalente a D3DXCreateTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, D3DX \_ default, D3DX \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, D3DX \_ default, D3DX \_ default, 0, **null**, **null**, ppTexture).

Le trame mipmap dispongono automaticamente di ogni livello riempito con la trama caricata.

Quando si caricano immagini in trame mipmap, alcuni dispositivi non sono in grado di passare a un'immagine 1x1 e questa funzione avrà esito negativo. In tal caso, è necessario caricare le immagini manualmente.

Si noti che una risorsa creata con questa funzione verrà inserita nella classe di memoria indicata da D3DPOOL \_ gestito.

Il filtro viene applicato automaticamente a una trama creata utilizzando questo metodo. Il filtro è equivalente a D3DX Filter D3DX del filtro \_ \_ \| \_ \_ di retinazione nel [ \_ filtro D3DX](d3dx-filter.md).

Per prestazioni ottimali quando si usa **D3DXCreateTextureFromFile**:

1.  Il ridimensionamento delle immagini e la conversione del formato in fase di caricamento possono essere lenti. Archiviare le immagini nel formato e nella risoluzione che verranno usate. Se l'hardware di destinazione richiede una potenza di due dimensioni, creare e archiviare immagini usando la potenza di due dimensioni.
2.  Prendere in considerazione l'uso di file di superficie DirectDraw (DDS). Poiché i file DDS possono essere usati per rappresentare qualsiasi formato di trama Direct3D 9, è molto facile per la lettura di D3DX. Inoltre, possono archiviare mipmap, in modo che sia possibile usare qualsiasi algoritmo di generazione mipmap per creare le immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[Funzioni di trama in D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
