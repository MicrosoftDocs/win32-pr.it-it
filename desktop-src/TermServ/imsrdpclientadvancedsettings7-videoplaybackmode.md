---
title: Proprietà VideoPlaybackMode di IMsRdpClientAdvancedSettings7
description: Specifica o recupera un valore che indica la modalità di riproduzione video.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà VideoPlaybackMode
- Servizi Desktop remoto proprietà VideoPlaybackMode, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà VideoPlaybackMode
- Servizi Desktop remoto proprietà VideoPlaybackMode, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f864224f402814ada268b9b7cbc85ec115a1fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400938"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>Proprietà IMsRdpClientAdvancedSettings7:: VideoPlaybackMode

Specifica o recupera un valore che indica la modalità di riproduzione video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>Valore proprietà

Valore che specifica la modalità di riproduzione video.

I valori possibili sono:

<dt>

1
</dt> <dd>

Modalità di riproduzione video predefinita. Quando la modalità di riproduzione video è impostata su questo valore, il reindirizzamento video è controllato dalla proprietà [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) . Quando la proprietà **AudioRedirectionMode** è impostata su **\_ \_ Reindirizzamento modalità audio**, il video viene decodificato e sottoposto a rendering nel client.

</dd> <dt>

0
</dt> <dd>

Il reindirizzamento della riproduzione video è disabilitato, anche quando [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) è impostato **su \_ \_ Reindirizzamento modalità audio**. In questa modalità, il video viene decodificato e sottoposto a rendering nel server Host sessione Desktop remoto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                             |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 è definito come 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





