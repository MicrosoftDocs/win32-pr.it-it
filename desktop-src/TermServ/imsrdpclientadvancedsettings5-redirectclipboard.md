---
title: Proprietà RedirectClipboard IMsRdpClientAdvancedSettings5
description: Imposta o recupera la configurazione per il reindirizzamento degli Appunti.
ms.assetid: c653f593-9912-4ade-a0a3-70d9afac2ab1
ms.tgt_platform: multiple
keywords:
- Proprietà RedirectClipboard Servizi Desktop remoto
- Proprietà RedirectClipboard Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings5
- Interfaccia IMsRdpClientAdvancedSettings5 Servizi Desktop remoto , proprietà RedirectClipboard
- Proprietà RedirectClipboard Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings6
- Interfaccia IMsRdpClientAdvancedSettings6 Servizi Desktop remoto , proprietà RedirectClipboard
- Proprietà RedirectClipboard Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings7
- Interfaccia IMsRdpClientAdvancedSettings7 Servizi Desktop remoto , proprietà RedirectClipboard
- Proprietà RedirectClipboard Servizi Desktop remoto, interfaccia IMsRdpClientAdvancedSettings8
- Interfaccia IMsRdpClientAdvancedSettings8 Servizi Desktop remoto , proprietà RedirectClipboard
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectClipboard
- IMsRdpClientAdvancedSettings5.get_RedirectClipboard
- IMsRdpClientAdvancedSettings5.put_RedirectClipboard
- IMsRdpClientAdvancedSettings6.RedirectClipboard
- IMsRdpClientAdvancedSettings6.get_RedirectClipboard
- IMsRdpClientAdvancedSettings6.put_RedirectClipboard
- IMsRdpClientAdvancedSettings7.RedirectClipboard
- IMsRdpClientAdvancedSettings7.get_RedirectClipboard
- IMsRdpClientAdvancedSettings7.put_RedirectClipboard
- IMsRdpClientAdvancedSettings8.RedirectClipboard
- IMsRdpClientAdvancedSettings8.get_RedirectClipboard
- IMsRdpClientAdvancedSettings8.put_RedirectClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5847ef4ccb5798ea74cccecbcabbb04303df93f3cd9a8a6155cd94eabbc8a824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352285"
---
# <a name="imsrdpclientadvancedsettings5redirectclipboard-property"></a>Proprietà IMsRdpClientAdvancedSettings5::RedirectClipboard

Imposta o recupera la configurazione per il reindirizzamento degli Appunti.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectClipboard(
  [in]  VARIANT_BOOL fRedirectClipboard
);

HRESULT get_RedirectClipboard(
  [out] VARIANT_BOOL *pfRedirectClipboard
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la modalità di reindirizzamento degli Appunti **su TRUE** o **FALSE.** Se impostato su **TRUE,** la modalità di reindirizzamento degli Appunti è abilitata.

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

 

 





