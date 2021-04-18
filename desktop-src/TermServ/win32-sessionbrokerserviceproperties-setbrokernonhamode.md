---
title: Metodo SetBrokerNonHAMode della classe Win32_SessionBrokerServiceProperties
description: Esegue la migrazione dei dati dalla SQL Server centrale a un database locale. Consente inoltre di configurare il server Broker per l'utilizzo del database locale.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetBrokerNonHAMode
- Metodo SetBrokerNonHAMode Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301609"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo SetBrokerNonHAMode della \_ classe SessionBrokerServiceProperties Win32

Esegue la migrazione dei dati dalla SQL Server centrale a un database locale. Consente inoltre di configurare il server Broker per l'utilizzo del database locale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connStringToCentralDBRdcms* \[ in\]
</dt> <dd>

Stringa di connessione al database centrale.

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

 

 





