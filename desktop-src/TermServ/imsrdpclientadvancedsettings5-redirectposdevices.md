---
title: Proprietà RedirectPOSDevices di IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per il reindirizzamento del dispositivo del punto di servizio.
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto, proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto, proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto, proprietà RedirectPOSDevices
- Servizi Desktop remoto proprietà RedirectPOSDevices, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto, proprietà RedirectPOSDevices
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120402"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a>Proprietà IMsRdpClientAdvancedSettings5:: RedirectPOSDevices

Imposta o recupera la configurazione per il reindirizzamento del dispositivo del punto di servizio.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la modalità di reindirizzamento del dispositivo punto di servizio su **true** o **false**. Se impostato su **true**, la modalità di reindirizzamento del dispositivo del punto di servizio è abilitata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                         |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                   |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 è definito come FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





