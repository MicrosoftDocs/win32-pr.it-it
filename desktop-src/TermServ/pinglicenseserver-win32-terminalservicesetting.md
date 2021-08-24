---
title: Metodo PingLicenseServer della classe Win32_TerminalServiceSetting
description: PingLicenseServer non è più disponibile.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Metodo PingLicenseServer Servizi Desktop remoto
- Metodo PingLicenseServer Servizi Desktop remoto , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Servizi Desktop remoto , metodo PingLicenseServer
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
ms.openlocfilehash: 4e5a52268073a076c5dada44b7f34c6a6b3e0c820c0b9819f65d23081f4f6c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866101"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo PingLicenseServer della classe TerminalServiceSetting Win32 \_

\[**PingLicenseServer** non è più disponibile per l'uso a Windows Server 2008 R2.\]

**Windows Server 2008:** Esegue il ping del server licenze per determinare se si tratta di un server licenze valido.

## <a name="syntax"></a>Sintassi


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NomeServer* \[ Pollici\]
</dt> <dd>

Nome del server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

<dl> <dt>

**S \_ OK**
</dt> <dd>

Il server è un server licenze valido.

</dd> <dt>

**S \_ FALSE**
</dt> <dd>

Il server licenze non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

