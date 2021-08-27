---
description: L'interfaccia ID3DXRenderToEnvMap viene usata per generalizzare il processo di rendering nelle mappe dell'ambiente.
ms.assetid: d72db260-5493-4381-9269-521ad333f0b2
title: Interfaccia ID3DXRenderToEnvMap (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94fc32654ca5bea81538a5dc56e7ca6b391287703a4a96dfccf62ceae497766a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095771"
---
# <a name="id3dxrendertoenvmap-interface"></a>Interfaccia ID3DXRenderToEnvMap

L'interfaccia ID3DXRenderToEnvMap viene usata per generalizzare il processo di rendering nelle mappe dell'ambiente.

## <a name="members"></a>Membri

**L'interfaccia ID3DXRenderToEnvMap** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXRenderToEnvMap** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXRenderToEnvMap** include questi metodi.



| Metodo                                                          | Descrizione                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginCube**](id3dxrendertoenvmap--begincube.md)             | Avviare il rendering di una mappa di ambiente cubica.<br/>                                                                                                                                    |
| [**BeginHemisphere**](id3dxrendertoenvmap--beginhemisphere.md) | Avviare il rendering di una mappa dell'ambiente emisferico.<br/>                                                                                                                              |
| [**BeginParabolic**](id3dxrendertoenvmap--beginparabolic.md)   | Avviare il rendering di una mappa dell'ambiente parabolico.<br/>                                                                                                                                |
| [**BeginSphere**](id3dxrendertoenvmap--beginsphere.md)         | Avviare il rendering di una mappa dell'ambiente sferica.<br/>                                                                                                                                |
| [**Fine**](id3dxrendertoenvmap--end.md)                         | Ripristinare tutte le destinazioni di rendering e, se necessario, comporre tutti i visi sottoposti a rendering nella superficie della mappa dell'ambiente.<br/>                                                                           |
| [**Viso**](id3dxrendertoenvmap--face.md)                       | Avviare il disegno di ogni viso di una mappa dell'ambiente.<br/>                                                                                                                              |
| [**GetDesc**](id3dxrendertoenvmap--getdesc.md)                 | Recupera la descrizione della superficie di rendering.<br/>                                                                                                                                      |
| [**GetDevice**](id3dxrendertoenvmap--getdevice.md)             | Recupera il dispositivo Direct3D associato alla mappa dell'ambiente.<br/>                                                                                                                    |
| [**OnLostDevice**](id3dxrendertoenvmap--onlostdevice.md)       | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/> |
| [**OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md)     | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Una mappa dell'ambiente viene usata per la geometria della scena della mappa di trama per fornire una scena più sofisticata senza usare una geometria complessa. Questa interfaccia supporta la creazione di superfici per i tipi di geometria seguenti: cubo, sfera semiferica o emisferica, parabolica o sfera.

**L'interfaccia ID3DXRenderToEnvMap** viene ottenuta chiamando la [**funzione D3DXCreateRenderToEnvMap.**](d3dxcreaterendertoenvmap.md)

Il tipo LPD3DXRenderToEnvMap è definito come puntatore **all'interfaccia ID3DXRenderToEnvMap.**


```
typedef interface ID3DXRenderToEnvMap ID3DXRenderToEnvMap;
typedef interface ID3DXRenderToEnvMap *LPD3DXRenderToEnvMap;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
