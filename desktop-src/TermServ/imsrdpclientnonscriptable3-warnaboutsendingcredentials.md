---
title: Proprietà WarnAboutSendingCredentials di IMsRdpClientNonScriptable3
description: Specifica o recupera un valore che indica se nella finestra di dialogo avviso di sicurezza deve essere incluso un avviso relativo all'invio di credenziali al server remoto prima di avviare una sessione.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
- Servizi Desktop remoto proprietà WarnAboutSendingCredentials, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà WarnAboutSendingCredentials
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
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301302"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>Proprietà IMsRdpClientNonScriptable3:: WarnAboutSendingCredentials

Specifica o recupera un valore che indica se nella finestra di dialogo avviso di sicurezza deve essere incluso un avviso relativo all'invio di credenziali al server remoto prima di avviare una sessione.

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

Specifica se la finestra di dialogo avviso di sicurezza deve includere un avviso sull'invio di credenziali al server remoto prima di avviare una sessione.

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

 

 





