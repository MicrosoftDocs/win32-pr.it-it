---
title: Metodo UpdateDirectConnectLicenseServer della classe Win32_TerminalServiceSetting
description: UpdateDirectConnectLicenseServer non è più disponibile.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UpdateDirectConnectLicenseServer
- Metodo UpdateDirectConnectLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301744"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Metodo UpdateDirectConnectLicenseServer della \_ classe TerminalServiceSetting Win32

\[**UpdateDirectConnectLicenseServer** non è più disponibile per l'uso a partire da Windows Server 2008 R2.\]

**Windows Server 2008:** Aggiorna l'elenco dei server licenze di individuazione. L'elenco dei server è delimitato da punti e virgola (";").

## <a name="syntax"></a>Sintassi


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*LicenseServerList* \[ in\]
</dt> <dd>

Elenco dei server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

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

 

