---
title: Proprietà IMsTscAx UserName
description: Specifica le credenziali di accesso del nome utente.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Servizi Desktop remoto
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsTscAx
- Interfaccia IMsTscAx Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient
- Interfaccia IMsRdpClient Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient2
- Interfaccia IMsRdpClient2 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient3
- Interfaccia IMsRdpClient3 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient4
- Interfaccia IMsRdpClient4 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto proprietà , UserName
- Proprietà UserName Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto proprietà , UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 609619a012c9eea865a275bc6ee86cfc06c798ba27902636f9d5f792b8cb0dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770881"
---
# <a name="imstscaxusername-property"></a>Proprietà IMsTscAx::UserName

Specifica le credenziali di accesso del nome utente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a>Valore proprietà

Nuovo nome utente.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

L'impostazione **della proprietà UserName** è facoltativa. Se non viene specificato, l'utente può specificare un nome utente quando viene visualizzata la finestra Windows di dialogo Accesso remoto durante la connessione.

Questa proprietà può essere impostata solo se il controllo non si trova nello stato connesso. Restituisce **E \_ FAIL** se viene chiamato quando il controllo è connesso. È possibile controllare se il controllo è connesso rispondendo agli eventi di connessione in [**IMsTscAxEvents**](imstscaxevents-interface.md) o esaminando la [**proprietà Connected.**](imstscax-connected.md)

Il **metodo della proprietà get \_ UserName** alloca la memoria necessaria per il buffer a cui punta il *parametro pVersion.* La chiamata alle applicazioni C/C++ deve liberare la memoria con una chiamata alla [**funzione SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) Questa operazione non è necessaria per i client Visual Basic e di scripting.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx è definito come 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

