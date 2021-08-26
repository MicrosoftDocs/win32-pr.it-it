---
title: Metodo PingSessionDirectory della classe Win32_TSSessionDirectory
description: Controlla se il server Connessione Desktop remoto Broker (Gestore connessione Desktop remoto) è disponibile.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Metodo PingSessionDirectory Servizi Desktop remoto
- Metodo PingSessionDirectory Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto , metodo PingSessionDirectory
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d26afbf26ab637dd58d8249ee822e152feefd948079f97c6e0adb876b4c7f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988841"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a>Metodo PingSessionDirectory della classe \_ TSSessionDirectory Win32

Controlla se il server Connessione Desktop remoto Broker (Gestore connessione Desktop remoto) è disponibile.

## <a name="syntax"></a>Sintassi


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NomeServer* \[ Pollici\]
</dt> <dd>

Tipo: **stringa**

Nome del server Gestore connessione Desktop remoto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

