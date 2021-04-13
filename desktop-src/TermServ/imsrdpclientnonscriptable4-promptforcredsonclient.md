---
title: Proprietà PromptForCredsOnClient di IMsRdpClientNonScriptable4
description: Specifica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà PromptForCredsOnClient
- Servizi Desktop remoto proprietà PromptForCredsOnClient, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400742"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a>IMsRdpClientNonScriptable4::P proprietà romptForCredsOnClient

Specifica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a>Valore proprietà

Imposta un valore che indica se il controllo client visualizza una finestra di dialogo in cui vengono richieste le credenziali.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 è definito come f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





