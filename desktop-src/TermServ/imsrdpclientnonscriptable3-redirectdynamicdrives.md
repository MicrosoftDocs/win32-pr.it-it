---
title: Proprietà RedirectDynamicDrives IMsRdpClientNonScriptable3
description: Specifica o recupera se le unità Plug and Play (PnP) associate dinamicamente che vengono enumerate durante una sessione sono disponibili per il reindirizzamento.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Proprietà RedirectDynamicDrives Servizi Desktop remoto
- Proprietà RedirectDynamicDrives Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto , proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto , interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto , proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto , oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto , oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto , oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto , oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto proprietà RedirectDynamicDrives
- Proprietà RedirectDynamicDrives Servizi Desktop remoto , oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto proprietà RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199f8fcf8e114cfb8febd05631e49de97aab01a69ca9397bc7d15539ad819d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001105"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>Proprietà IMsRdpClientNonScriptable3::RedirectDynamicDrives

Specifica o recupera se le unità Plug and Play (PnP) associate dinamicamente che vengono enumerate durante una sessione sono disponibili per il reindirizzamento.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se le unità PnP collegate dinamicamente enumerate durante una sessione sono disponibili per il reindirizzamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 è definito come b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





