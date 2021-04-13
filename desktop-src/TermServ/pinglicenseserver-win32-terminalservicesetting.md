---
title: Metodo PingLicenseServer della classe Win32_TerminalServiceSetting
description: PingLicenseServer non è più disponibile.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo PingLicenseServer
- Metodo PingLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400582"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo PingLicenseServer della \_ classe TerminalServiceSetting Win32

\[**PingLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]

**Windows Server 2008:** Effettua il ping del server licenze per determinare se si tratta di un server licenze valido.

## <a name="syntax"></a>Sintassi


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nomeserver* \[ in\]
</dt> <dd>

Nome del server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>

**\_OK**
</dt> <dd>

Il server è un server licenze valido.

</dd> <dt>

**S \_ false**
</dt> <dd>

Il server licenze non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

