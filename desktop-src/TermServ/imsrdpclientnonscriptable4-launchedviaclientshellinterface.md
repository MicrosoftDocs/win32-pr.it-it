---
title: Proprietà LaunchedViaClientShellInterface di IMsRdpClientNonScriptable4
description: Specifica se l'utente ha avviato il controllo client utilizzando l'interfaccia Desktop remoto Accesso Web (RD Accesso Web).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient5
- Oggetto MsRdpClient5 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient6
- Oggetto MsRdpClient6 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient7
- Oggetto MsRdpClient7 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient8
- Oggetto MsRdpClient8 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
- Servizi Desktop remoto proprietà LaunchedViaClientShellInterface, oggetto MsRdpClient9
- Oggetto MsRdpClient9 Servizi Desktop remoto, proprietà LaunchedViaClientShellInterface
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
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964424"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>Proprietà IMsRdpClientNonScriptable4:: LaunchedViaClientShellInterface

Specifica se l'utente ha avviato il controllo client utilizzando l'interfaccia Desktop remoto Accesso Web (RD Accesso Web).

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

Imposta la proprietà **LaunchedViaClientShellInterface** .

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

 

 





