---
description: Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni con fotogrammi chiave.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Interfaccia ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323480"
---
# <a name="id3dxkeyframedanimationset-interface"></a>Interfaccia ID3DXKeyframedAnimationSet

Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni con fotogrammi chiave.

## <a name="members"></a>Membri

L'interfaccia **ID3DXKeyframedAnimationSet** eredita da [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXKeyframedAnimationSet** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXKeyframedAnimationSet** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Comprimere**](id3dxkeyframedanimationset--compress.md)                                 | Trasforma le animazioni in un set di animazioni in un formato compresso e restituisce un puntatore al buffer che archivia i dati compressi.<br/> |
| [**GetCallbackKey**](id3dxkeyframedanimationset--getcallbackkey.md)                     | Ottiene informazioni su un callback specifico nel set di animazioni.<br/>                                                                        |
| [**GetCallbackKeys**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.<br/>                                                                     |
| [**GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | Ottiene il numero di chiavi di callback nel set di animazioni.<br/>                                                                                  |
| [**GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | Ottiene il numero di chiavi di rotazione nell'animazione del fotogramma chiave specificata.<br/>                                                                  |
| [**GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | Ottiene il numero di chiavi di scala nell'animazione del fotogramma chiave specificata.<br/>                                                                     |
| [**GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | Ottiene il numero di chiavi di traslazione nell'animazione del fotogramma chiave specificata.<br/>                                                               |
| [**GetPlaybackType**](id3dxkeyframedanimationset--getplaybacktype.md)                   | Ottiene il tipo del ciclo di riproduzione del set di animazioni.<br/>                                                                                       |
| [**GetRotationKey**](id3dxkeyframedanimationset--getrotationkey.md)                     | Ottenere le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.<br/>                                                                 |
| [**GetRotationKeys**](id3dxkeyframedanimationset--getrotationkeys.md)                   | Compila una matrice con i dati della chiave rotazionale usati per l'animazione del fotogramma chiave.<br/>                                                                   |
| [**GetScaleKey**](id3dxkeyframedanimationset--getscalekey.md)                           | Ottenere informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.<br/>                                                                    |
| [**GetScaleKeys**](id3dxkeyframedanimationset--getscalekeys.md)                         | Compila una matrice con i dati della chiave della scala usati per l'animazione del fotogramma chiave.<br/>                                                                        |
| [**GetSourceTicksPerSecond**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | Ottiene il numero di cicli del fotogramma chiave di animazione che si verificano al secondo.<br/>                                                                     |
| [**GetTranslationKey**](id3dxkeyframedanimationset--gettranslationkey.md)               | Ottiene le informazioni di conversione per un fotogramma chiave specifico nel set di animazioni.<br/>                                                              |
| [**GetTranslationKeys**](id3dxkeyframedanimationset--gettranslationkeys.md)             | Compila una matrice con i dati della chiave di conversione utilizzati per l'animazione del fotogramma chiave.<br/>                                                                |
| [**RegisterAnimationSRTKeys**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | Registrare i dati del fotogramma chiave SRT (scale, Rotate e translate) per un'animazione.<br/>                                                        |
| [**SetCallbackKey**](id3dxkeyframedanimationset--setcallbackkey.md)                     | Imposta le informazioni su un callback specifico nel set di animazioni.<br/>                                                                        |
| [**SetRotationKey**](id3dxkeyframedanimationset--setrotationkey.md)                     | Impostare le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.<br/>                                                                 |
| [**SetScaleKey**](id3dxkeyframedanimationset--setscalekey.md)                           | Impostare le informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.<br/>                                                                    |
| [**SetTranslationKey**](id3dxkeyframedanimationset--settranslationkey.md)               | Impostare le informazioni di traduzione per un fotogramma chiave specifico nel set di animazioni.<br/>                                                              |
| [**UnregisterAnimation**](id3dxkeyframedanimationset--unregisteranimation.md)           | Rimuovere i dati di animazione dal set di animazioni.<br/>                                                                                       |
| [**UnregisterRotationKey**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | Rimuove i dati di rotazione in corrispondenza del fotogramma chiave specificato.<br/>                                                                                   |
| [**UnregisterScaleKey**](id3dxkeyframedanimationset--unregisterscalekey.md)             | Rimuove i dati della scala in corrispondenza del fotogramma chiave specificato.<br/>                                                                                      |
| [**UnregisterTranslationKey**](id3dxkeyframedanimationset--unregistertranslationkey.md) | Rimuove i dati di traduzione in corrispondenza del fotogramma chiave specificato.<br/>                                                                                |



 

## <a name="remarks"></a>Commenti

Creare un set di animazioni con fotogramma chiave con [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).

Il tipo LPD3DXKEYFRAMEDANIMATIONSET è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




