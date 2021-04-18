---
title: Metodo CreateWinstation della classe Win32_TerminalServiceSetting
description: Crea un nuovo stack del listener in base alla combinazione univoca di nome del listener e NIC.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateWinstation
- Metodo CreateWinstation Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301129"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a>Metodo CreateWinstation della \_ classe TerminalServiceSetting Win32

Il metodo **CreateWinstation** crea un nuovo stack del listener in base alla combinazione univoca del nome del listener e della scheda di interfaccia di rete.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome del listener.

</dd> <dt>

*WinstaDriverName* \[ in\]
</dt> <dd>

Nome del driver WinStation.

</dd> <dt>

*LanaID* \[ in\]
</dt> <dd>

Numero di scheda di rete locale NetBIOS (LANA) per la scheda di interfaccia di rete.

</dd> </dl>

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

 

