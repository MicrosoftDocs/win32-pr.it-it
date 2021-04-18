---
description: Include le impostazioni possibili per i criteri di accesso automatico.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Enumerazione WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307091"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>Enumerazione WinHttpRequestAutoLogonPolicy

L'enumerazione **WinHttpRequestAutoLogonPolicy** include le possibili impostazioni per il [criterio di accesso automatico](authentication-in-winhttp.md).

## <a name="syntax"></a>Sintassi


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ sempre**
</dt> <dd>

Un accesso autenticato, usando le credenziali predefinite, viene eseguito per tutte le richieste.

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**\_OnlyIfBypassProxy AutoLogonPolicy**
</dt> <dd>

Un accesso autenticato, utilizzando le credenziali predefinite, viene eseguito solo per le richieste nella Intranet locale. La Intranet locale viene considerata come qualsiasi server nell'elenco proxy bypass nella configurazione del proxy corrente.

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ mai**
</dt> <dd>

L'autenticazione non viene utilizzata automaticamente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostare i criteri di accesso automatici, chiamare il metodo [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) e specificare una delle costanti precedenti.

> [!Note]  
> Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]<br/>            |
| Server minimo supportato<br/> | Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]<br/>         |
| Componente ridistribuibile<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Versioni WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




