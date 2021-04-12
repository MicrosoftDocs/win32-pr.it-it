---
description: Questa interfaccia incapsula le funzionalità minime necessarie per un'animazione impostata da un controller di animazione.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interfaccia ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235201"
---
# <a name="id3dxanimationset-interface"></a>Interfaccia ID3DXAnimationSet

Questa interfaccia incapsula le funzionalità minime necessarie per un'animazione impostata da un controller di animazione. Gli utenti avanzati potrebbero voler implementare questa interfaccia per soddisfare le proprie esigenze specializzate; per la maggior parte degli utenti, tuttavia, devono essere sufficienti le interfacce [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) e [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) derivate.

## <a name="members"></a>Membri

L'interfaccia **ID3DXAnimationSet** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationSet** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXAnimationSet** dispone di questi metodi.



| Metodo                                                                        | Descrizione                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetAnimationIndexByName**](id3dxanimationset--getanimationindexbyname.md) | Ottiene l'indice di un'animazione, dato il relativo nome.<br/>                        |
| [**GetAnimationNameByIndex**](id3dxanimationset--getanimationnamebyindex.md) | Ottiene il nome di un'animazione, dato il relativo indice.<br/>                        |
| [**GetCallback**](id3dxanimationset--getcallback.md)                         | Ottiene informazioni su un callback specifico nel set di animazioni.<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | Ottiene il nome del set di animazioni.<br/>                                           |
| [**GetNumAnimations**](id3dxanimationset--getnumanimations.md)               | Ottiene il numero di animazioni nel set di animazioni.<br/>                    |
| [**GetPeriod**](id3dxanimationset--getperiod.md)                             | Ottiene il periodo del set di animazioni.<br/>                                  |
| [**GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)         | Restituisce la posizione dell'ora nell'intervallo di tempo locale di un set di animazioni.<br/>      |
| [**GetSRT**](id3dxanimationset--getsrt.md)                                   | Ottiene i valori di scala, rotazione e traslazione del set di animazioni.<br/> |



 

## <a name="remarks"></a>Commenti

Un set di animazioni è costituito da animazioni per molti nodi per la stessa animazione.

Il tipo LPD3DXANIMATIONSET è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
