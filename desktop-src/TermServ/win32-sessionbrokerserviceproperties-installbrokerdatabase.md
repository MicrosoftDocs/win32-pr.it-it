---
title: Metodo InstallBrokerDatabase della classe Win32_SessionBrokerServiceProperties
description: Installa un database gestore connessione Desktop remoto in un server SQL centrale.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallBrokerDatabase
- Metodo InstallBrokerDatabase Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo InstallBrokerDatabase
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740199"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo InstallBrokerDatabase della \_ classe SessionBrokerServiceProperties Win32

Installa un database gestore connessione Desktop remoto in un server SQL centrale.

## <a name="syntax"></a>Sintassi


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newDbFilePath* \[ in\]
</dt> <dd>

nuovo percorso del file di database.

</dd> <dt>

*connStringToCentralDBMaster* \[ in\]
</dt> <dd>

Stringa di connessione al Master di database centrale.

</dd> <dt>

*centralRdcmsDbName* \[ in\]
</dt> <dd>

Nome del database centrale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SessionBrokerServiceProperties Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





