---
title: Proprietà IMsRdpClientNonScriptable5 AllowPromptingForCredentials
description: Specifica se il controllo Desktop remoto ActiveX può richiedere le credenziali all'utente.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Proprietà AllowPromptingForCredentials Servizi Desktop remoto
- Proprietà AllowPromptingForCredentials Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto proprietà , AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea0fb854b5bb12533032cd6608228d81584cd8d9f4e99bccd8a5ba76b624f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138754"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>Proprietà IMsRdpClientNonScriptable5::AllowPromptingForCredentials

Specifica se il controllo Desktop remoto ActiveX può richiedere le credenziali all'utente. Se questa proprietà contiene **VARIANT \_ TRUE,** all'utente possono essere richieste le credenziali. Se questa proprietà contiene **VARIANT \_ FALSE,** all'utente non è possibile richiedere le credenziali.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a>Valore proprietà

Specifica il nuovo valore della proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 è definito come 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





