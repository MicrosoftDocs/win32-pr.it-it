---
title: Metodo InstallBrokerDatabase della classe Win32_SessionBrokerServiceProperties
description: Installa un database di Gestore connessione Desktop remoto in un server SQL centrale.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- Metodo InstallBrokerDatabase Servizi Desktop remoto
- Metodo InstallBrokerDatabase Servizi Desktop remoto , Win32_SessionBrokerServiceProperties classe
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto , metodo InstallBrokerDatabase
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
ms.openlocfilehash: 4e77a34c70fbf06bac5501c8cacddce9feb9211d1fe21c1ef30fe429d3e75308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422451"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo InstallBrokerDatabase della classe \_ Win32 SessionBrokerServiceProperties

Installa un database di Gestore connessione Desktop remoto in un server SQL centrale.

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

*newDbFilePath* \[ Pollici\]
</dt> <dd>

nuovo percorso del file di database.

</dd> <dt>

*connStringToCentralDBMaster* \[ Pollici\]
</dt> <dd>

Stringa di connessione al database master centrale.

</dd> <dt>

*centralRdcmsDbName* \[ Pollici\]
</dt> <dd>

Nome del database centrale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





