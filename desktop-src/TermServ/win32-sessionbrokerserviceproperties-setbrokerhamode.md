---
title: Metodo SetBrokerHAMode della classe Win32_SessionBrokerServiceProperties
description: Esegue la migrazione dei dati da un database WID locale al nuovo database basato su SQL Server. Configura inoltre il server Broker per l'utilizzo del server SQL centrale.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetBrokerHAMode
- Metodo SetBrokerHAMode Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119766"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo SetBrokerHAMode della \_ classe SessionBrokerServiceProperties Win32

Esegue la migrazione dei dati da un database WID locale al nuovo database basato su SQL Server. Configura inoltre il server Broker per l'utilizzo del server SQL centrale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connStringToCentralDBRdcms* \[ in\]
</dt> <dd>

Stringa di connessione al database centrale.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ in\]
</dt> <dd>

Stringa di connessione secondaria al database centrale.

**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ in\]
</dt> <dd>

Nome DNS del broker.

</dd> <dt>

*activeBrokerName* \[ in\]
</dt> <dd>

Nome del broker attivo.

**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.

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

 

 





