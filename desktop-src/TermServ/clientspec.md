---
title: Enumerazione ClientSpec
description: Utilizzato con la proprietà ClientProtocolSpec per specificare il protocollo desktop remoto utilizzato tra il client e il server.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto enumerazione ClientSpec
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301133"
---
# <a name="clientspec-enumeration"></a>Enumerazione ClientSpec

Utilizzato con la proprietà [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) per specificare il protocollo desktop remoto utilizzato tra il client e il server.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**
</dt> <dd>

Il protocollo è il protocollo completo di Windows 8 Desktop remoto.

</dd> <dt>

<span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**
</dt> <dd>

Il protocollo è limitato all'uso del codec Windows 7 con SP1 RemoteFX e di una cache più piccola. Tutti gli altri codec sono disabilitati. Questo protocollo ha il footprint di memoria più piccolo.

</dd> <dt>

<span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**
</dt> <dd>

Il protocollo è identico a **FullMode**, con la differenza che usa una cache più piccola.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





