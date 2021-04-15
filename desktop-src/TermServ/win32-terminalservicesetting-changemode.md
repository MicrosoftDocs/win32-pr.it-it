---
title: Metodo ChangeMode della classe Win32_TerminalServiceSetting
description: Il metodo ChangeMode imposta il tipo di licenza del server di host sessione Desktop remoto (host sessione Desktop remoto) corrente.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ChangeMode
- Metodo ChangeMode Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400568"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Metodo ChangeMode della \_ classe TerminalServiceSetting Win32

Il metodo **ChangeMode** imposta il tipo di licenza del server di host sessione Desktop remoto (host sessione Desktop remoto) corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicensingType* \[ in\]
</dt> <dd>

Tipo di licenza da impostare in base alla modalità server Host sessione Desktop remoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Server Host sessione Desktop remoto personale.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Desktop remoto per l'amministrazione.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Per dispositivo/per postazione. Valido per i server applicazioni.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Per utente. Valido per i server applicazioni.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

