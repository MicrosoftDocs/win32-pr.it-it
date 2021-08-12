---
title: Proprietà IMsRdpClientNonScriptable4 AllowCredentialSaving
description: Specifica se nella finestra di dialogo delle credenziali viene visualizzata una casella di controllo che consente il salvataggio delle credenziali.
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- Impostazione della proprietà AllowCredentialSaving Servizi Desktop remoto
- Proprietà AllowCredentialSaving Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto , proprietà AllowCredentialSaving
- Proprietà AllowCredentialSaving Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto , proprietà AllowCredentialSaving
- Proprietà AllowCredentialSaving Servizi Desktop remoto , oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto proprietà , AllowCredentialSaving
- Proprietà AllowCredentialSaving Servizi Desktop remoto , oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto proprietà , AllowCredentialSaving
- Proprietà AllowCredentialSaving Servizi Desktop remoto , oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto proprietà , AllowCredentialSaving
- Proprietà AllowCredentialSaving Servizi Desktop remoto , oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto proprietà , AllowCredentialSaving
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cca6f61b8cbcc315eb93e6e9c3ab0f89684e4d29c3fcb8313af0198ee594cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607733"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a>Proprietà IMsRdpClientNonScriptable4::AllowCredentialSaving

Specifica se nella finestra di dialogo delle credenziali viene visualizzata una casella di controllo che consente il salvataggio delle credenziali.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a>Valore proprietà

Specifica se nella finestra di dialogo delle credenziali viene visualizzata una casella di controllo che consente il salvataggio delle credenziali.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

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

 

 





