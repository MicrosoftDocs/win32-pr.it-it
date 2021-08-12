---
title: Proprietà IMsRdpClientNonScriptable4 LaunchedViaClientShellInterface
description: Specifica se l'utente ha avviato il controllo client usando l'interfaccia Desktop remoto Accesso Web (Accesso Web Desktop remoto).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto , oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto , oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto , oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto , oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
- Proprietà LaunchedViaClientShellInterface Servizi Desktop remoto , oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto proprietà , LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf4b3af34d274ae2ebfc34aed2a4256272daca2365966795de14d6b156562d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607589"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>Proprietà IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface

Specifica se l'utente ha avviato il controllo client usando l'interfaccia Desktop remoto Accesso Web (Accesso Web Desktop remoto).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la **proprietà LaunchedViaClientShellInterface.**

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

 

 





