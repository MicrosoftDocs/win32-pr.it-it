---
title: Metodo ExplicitLogon della classe Win32_TSLogonSetting
description: Il metodo ExplicitLogon imposta le credenziali da usare per l'autenticazione.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Metodo ExplicitLogon Servizi Desktop remoto
- Metodo ExplicitLogon Servizi Desktop remoto , Win32_TSLogonSetting classe
- Win32_TSLogonSetting classe Servizi Desktop remoto , metodo ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7303f06967d26276c7b43e06109cd9b37d664b960946afdffbb4f6a5a7c18821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137784"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Metodo ExplicitLogon della classe \_ TSLogonSetting Win32

Il **metodo ExplicitLogon** imposta le credenziali da usare per l'autenticazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Credenziali di accesso del nome utente.

</dd> <dt>

*Dominio* \[ Pollici\]
</dt> <dd>

Credenziali di accesso al dominio.

</dd> <dt>

*Password* \[ Pollici\]
</dt> <dd>

Credenziali di accesso della password.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere . Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

