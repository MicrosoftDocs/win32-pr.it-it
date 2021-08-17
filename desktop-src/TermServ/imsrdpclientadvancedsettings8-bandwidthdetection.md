---
title: Proprietà BandwidthDetection IMsRdpClientAdvancedSettings8
description: Specifica se vengono rilevate automaticamente modifiche alla larghezza di banda.
ms.assetid: 30b2b7b3-9050-4a11-9929-2ad1dbf5ed2d
ms.tgt_platform: multiple
keywords:
- Proprietà BandwidthDetection Servizi Desktop remoto
- Proprietà BandwidthDetection Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà BandwidthDetection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ab6fbe8291c0318e378add8041d0e2d2d0f30b6ee1e298c3a43a6a0ccd430c31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138784"
---
# <a name="imsrdpclientadvancedsettings8bandwidthdetection-property"></a>Proprietà IMsRdpClientAdvancedSettings8::BandwidthDetection

Specifica se vengono rilevate automaticamente modifiche alla larghezza di banda.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BandwidthDetection(
  [in]          VARIANT_BOOL fAutodetect
);

HRESULT get_BandwidthDetection(
  [out, retval] VARIANT_BOOL *pfAutodetect
);
```



## <a name="property-value"></a>Valore proprietà

**VARIANT \_ TRUE se** le modifiche alla larghezza di banda vengono rilevate automaticamente o **VARIANT FALSE in \_ caso** contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





