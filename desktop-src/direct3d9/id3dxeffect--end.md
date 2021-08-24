---
description: Termina una tecnica attiva.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: Metodo ID3DXEffect::End (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6c93dc98febe2f5e539d3be678322860fe14069c2f8bf6b75cc42864b922e1f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748661"
---
# <a name="id3dxeffectend-method"></a>Metodo ID3DXEffect::End

Termina una tecnica attiva.

## <a name="syntax"></a>Sintassi


```C++
HRESULT End();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Questo metodo restituisce sempre il valore S \_ OK.

## <a name="remarks"></a>Commenti

Tutto il rendering in un effetto viene eseguito all'interno di una coppia corrispondente di [**chiamate ID3DXEffect::Begin**](id3dxeffect--begin.md) **e ID3DXEffect::End.** Dopo il rendering di tutti i passaggi, è necessario chiamare **ID3DXEffect::End** per terminare la tecnica attiva. Il sistema degli effetti risponde usando il blocco di stato creato quando è stato chiamato **ID3DXEffect::Begin,** per ripristinare automaticamente lo stato della pipeline prima di **ID3DXEffect::Begin.**

Per impostazione predefinita, il sistema degli effetti si occupa del salvataggio dello stato prima di una tecnica e del ripristino dello stato dopo una tecnica. Se si sceglie di disabilitare questa funzionalità di salvataggio e ripristino, vedere [D3DXFX \_ DONOTSAVESAMPLERSTATE.](d3dxfx.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




