---
description: Prepara un dispositivo per il disegno di linee.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: Metodo ID3DXLine::Begin (D3dx9core.h)
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
ms.openlocfilehash: 9daa65558c58849d406056ce3358c26fdf2ce1c604342f993babe6af553d130f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629651"
---
# <a name="id3dxlinebegin-method"></a>Metodo ID3DXLine::Begin

Prepara un dispositivo per il disegno di linee.

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

La **chiamata a ID3DXLine::Begin** è facoltativa. Se viene chiamato all'esterno di una sequenza ID3DXLine::Begin/ID3DXLine::End, le funzioni di disegno chiameranno internamente ID3DXLine::Begin e ID3DXLine::End. Per evitare un sovraccarico aggiuntivo, questo metodo deve essere usato se più di una funzione di disegno verrà chiamata in successione.

Questo metodo deve essere chiamato dall'interno di una sequenza [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9::EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene)

ID3DXLine::Begin non può essere usato come sostituzione di [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) o [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
