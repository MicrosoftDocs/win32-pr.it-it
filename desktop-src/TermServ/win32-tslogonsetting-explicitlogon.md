---
title: Metodo ExplicitLogon della classe Win32_TSLogonSetting
description: Il metodo ExplicitLogon imposta le credenziali da usare per l'autenticazione.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ExplicitLogon
- Metodo ExplicitLogon Servizi Desktop remoto, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Servizi Desktop remoto, metodo ExplicitLogon
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
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400774"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Metodo ExplicitLogon della \_ classe TSLogonSetting Win32

Il metodo **ExplicitLogon** imposta le credenziali da usare per l'autenticazione.

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

*Nome utente* \[ in\]
</dt> <dd>

Credenziali di accesso del nome utente.

</dd> <dt>

*Dominio* \[ in\]
</dt> <dd>

Credenziali di accesso al dominio.

</dd> <dt>

*Password* \[ di in\]
</dt> <dd>

Credenziali di accesso alla password.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

