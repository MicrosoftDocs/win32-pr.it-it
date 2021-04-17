---
description: L'interfaccia ID3DXRenderToSurface viene utilizzata per generalizzare il processo di rendering nelle superfici.
ms.assetid: e9f2ca5e-faa3-45a8-94eb-16f354618e80
title: Interfaccia ID3DXRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 577e729e4e1a510dd24dc981b2b90bdca27dc0f9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355824"
---
# <a name="id3dxrendertosurface-interface"></a>Interfaccia ID3DXRenderToSurface

L'interfaccia ID3DXRenderToSurface viene utilizzata per generalizzare il processo di rendering nelle superfici.

## <a name="members"></a>Membri

L'interfaccia **ID3DXRenderToSurface** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXRenderToSurface** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXRenderToSurface** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                                                                                                                                     |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginScene**](id3dxrendertosurface--beginscene.md)       | Inizia una scena.<br/>                                                                                                                                                                      |
| [**EndScene**](id3dxrendertosurface--endscene.md)           | Termina una scena.<br/>                                                                                                                                                                        |
| [**Getdesc**](id3dxrendertosurface--getdesc.md)             | Recupera i parametri della superficie di rendering.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertosurface--getdevice.md)         | Recupera il dispositivo Direct3D associato alla superficie di rendering.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertosurface--onlostdevice.md)   | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertosurface--onresetdevice.md) | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Le superfici possono essere usate in diversi modi, tra cui le destinazioni di rendering, il rendering fuori schermo o il rendering in trame.

Una superficie può essere configurata usando un viewport separato usando il metodo [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md) per fornire una visualizzazione di rendering personalizzata. Se la superficie non è una destinazione di rendering, viene utilizzata una destinazione di rendering compatibile e il risultato viene copiato nell'area alla fine della scena.

L'interfaccia **ID3DXRenderToSurface** viene ottenuta chiamando la funzione [**D3DXCreateRenderToSurface**](d3dxcreaterendertosurface.md) .

Il tipo LPD3DXRENDERTOSURFACE è definito come puntatore all'interfaccia **ID3DXRenderToSurface** .


```
typedef interface ID3DXRenderToSurface ID3DXRenderToSurface;
typedef interface ID3DXRenderToSurface *LPD3DXRENDERTOSURFACE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
