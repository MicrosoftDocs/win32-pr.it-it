---
description: Prepara un dispositivo per il disegno delle linee.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'Metodo ID3DXLine:: begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323478"
---
# <a name="id3dxlinebegin-method"></a>Metodo ID3DXLine:: Begin

Prepara un dispositivo per il disegno delle linee.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Begin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è D3D \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Commenti

La chiamata a **ID3DXLine:: Begin** è facoltativa. Se viene chiamato al di fuori di una sequenza ID3DXLine:: Begin/ID3DXLine:: end, le funzioni di estrazione chiameranno internamente ID3DXLine:: Begin e ID3DXLine:: end. Per evitare un sovraccarico aggiuntivo, questo metodo deve essere usato se più di una funzione di estrazione verrà chiamata successivamente.

Questo metodo deve essere chiamato dall'interno di una sequenza [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .

Impossibile utilizzare ID3DXLine:: Begin come sostituto di [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
