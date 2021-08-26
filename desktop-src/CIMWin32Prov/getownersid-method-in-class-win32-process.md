---
description: GetOwnerSid&\# 8194; Il metodo della classe WMI recupera l'ID di sicurezza (SID) per il proprietario di questo processo.
ms.assetid: f856b06c-8080-4145-a775-51361f741873
ms.tgt_platform: multiple
title: Metodo GetOwnerSid della Win32_Process classe
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
ms.openlocfilehash: 2884c0f1cd3cc6e32a2db1ab14824ba3112624002cb10f4d76782d622e069000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918381"
---
# <a name="getownersid-method-of-the-win32_process-class"></a>Metodo GetOwnerSid della classe Process \_ Win32

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwnerSid** recupera l'ID di sicurezza (SID) per il proprietario di questo processo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 GetOwnerSid(
  [out] string Sid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sid* \[ Cambio\]
</dt> <dd>

Restituisce il descrittore dell'ID di sicurezza per questo processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero (0) per indicare l'esito positivo. Qualsiasi altro numero indica un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Completamento riuscito** (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegi insufficienti** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non** valido (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Esempio

L'esempio di codice di PowerShell Trovare gli utenti connessi in un sistema remoto versione [2](https://Gallery.TechNet.Microsoft.Com/Find-the-logged-on-users-1161bd92) esegue una query sui computer remoti per vedere chi è connesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Processo \_ Win32**](win32-process.md)
</dt> </dl>

 

