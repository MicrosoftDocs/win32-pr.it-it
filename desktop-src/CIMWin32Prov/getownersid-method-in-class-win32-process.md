---
description: GetOwnerSid&\# 8194; Il metodo della classe WMI recupera l'ID di sicurezza (SID) per il proprietario del processo.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Metodo GetOwnerSid della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwnerSid
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c3ed34d132d363c0ce9f83511459ec40f340a06c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304683"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Metodo GetOwnerSid della classe di \_ processo Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** recupera l'ID di sicurezza (SID) per il proprietario del processo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SID* \[ di out\]
</dt> <dd>

Restituisce il descrittore dell'identificatore di sicurezza per questo processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento** completato (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegio insufficiente** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non valido** (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Esempio

Nell'esempio di codice [trovare gli utenti connessi in un sistema remoto/s versione 2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) PowerShell viene eseguita una query sui computer remoti per verificare chi ha eseguito l'accesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

