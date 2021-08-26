---
description: Valori guid (Globally Unique Identifier) che identificano i produttori di messaggi di debug.
ms.assetid: 85946D30-5E49-4E4B-AC25-394ABFF0DB11
title: DXGI_DEBUG_ID (DXGIDebug.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3642f8ece96a7a63ed6137eef14069a33a418511321a4df10cdd95e122e13397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068821"
---
# <a name="dxgi_debug_id"></a>DXGI \_ DEBUG \_ ID

Valori guid (Globally Unique Identifier) che identificano i produttori di messaggi di debug.



| Costante/valore                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_DEBUG_ALL"></span><span id="dxgi_debug_all"></span><dl> <dt>**DXGI \_ DEBUG \_ ALL**</dt> <dt>0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8</dt> </dl>       | Tutti gli oggetti Direct3D e DXGI e le app private.<br/>                                                                                     |
| <span id="DXGI_DEBUG_DX"></span><span id="dxgi_debug_dx"></span><dl> <dt>**DXGI \_ DEBUG \_ DX**</dt> <dt>0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64</dt> </dl>         | Oggetti Direct3D e DXGI.<br/>                                                                                                          |
| <span id="DXGI_DEBUG_DXGI"></span><span id="dxgi_debug_dxgi"></span><dl> <dt>**DXGI \_ DEBUG \_ DXGI**</dt> <dt>0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a</dt> </dl>   | DXGI.<br/>                                                                                                                               |
| <span id="DXGI_DEBUG_APP"></span><span id="dxgi_debug_app"></span><dl> <dt>**DXGI \_ DEBUG \_ DI APP**</dt> <dt>0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62</dt> </dl>         | App private. Tutti i messaggi aggiunti con [**IDXGIInfoQueue::AddApplicationMessage**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgiinfoqueue-addapplicationmessage).<br/> |
| <span id="DXGI_DEBUG_D3D11"></span><span id="dxgi_debug_d3d11"></span><dl> <dt>**DXGI \_ DEBUG \_ D3D11**</dt> <dt>0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f</dt> </dl> | Direct3D 11. Definito in D3D11SDKLayers.h.<br/>                                                                                           |



## <a name="remarks"></a>Commenti

Usare questi valori con [**l'interfaccia IDXGIInfoQueue.**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

``` syntax
typedef GUID DXGI_DEBUG_ID;

DEFINE_GUID(DXGI_DEBUG_ALL, 0xe48ae283, 0xda80, 0x490b, 0x87, 0xe6, 0x43, 0xe9, 0xa9, 0xcf, 0xda, 0x8);
DEFINE_GUID(DXGI_DEBUG_DX, 0x35cdd7fc, 0x13b2, 0x421d, 0xa5, 0xd7, 0x7e, 0x44, 0x51, 0x28, 0x7d, 0x64);
DEFINE_GUID(DXGI_DEBUG_DXGI, 0x25cddaa4, 0xb1c6, 0x47e1, 0xac, 0x3e, 0x98, 0x87, 0x5b, 0x5a, 0x2e, 0x2a);
DEFINE_GUID(DXGI_DEBUG_APP, 0x6cd6e01, 0x4219, 0x4ebd, 0x87, 0x9, 0x27, 0xed, 0x23, 0x36, 0xc, 0x62);

DEFINE_GUID(DXGI_DEBUG_D3D11, 0x4b99317b, 0xac39, 0x4aa6, 0xbb, 0xb, 0xba, 0xa0, 0x47, 0x84, 0x79, 0x8f);
```

Per usare uno di questi valori GUID, includere DXGIDebug.h nel codice e collegarsi a dxguid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                      |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>DXGIDebug.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti DXGI](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




