---
title: Proprietà IMsRdpClientNonScriptable3 WarnAboutSendingCredentials
description: Specifica o recupera se la finestra di dialogo di avviso di sicurezza deve includere un avviso relativo all'invio di credenziali al server remoto prima di avviare una sessione.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto , proprietà WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto , proprietà WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , oggetto MsRdpClient5
- Proprietà Dell'oggetto MsRdpClient5 Servizi Desktop remoto , WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto proprietà WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto proprietà WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto proprietà , WarnAboutSendingCredentials
- Proprietà WarnAboutSendingCredentials Servizi Desktop remoto , oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto proprietà WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48924b435e09b002992e6380ef130a1e11ca4961dbb0d3514b8c551f21f1b648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607680"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>Proprietà IMsRdpClientNonScriptable3::WarnAboutSendingCredentials

Specifica o recupera se la finestra di dialogo di avviso di sicurezza deve includere un avviso relativo all'invio di credenziali al server remoto prima di avviare una sessione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se la finestra di dialogo di avviso di sicurezza deve includere un avviso sull'invio di credenziali al server remoto prima di avviare una sessione.

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

 

 





