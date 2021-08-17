---
title: Metodo SetBrokerNonHAMode della classe Win32_SessionBrokerServiceProperties
description: Esegue la migrazione dei dati dal SQL Server centrale a un database locale. Configura anche il server broker per l'uso del database locale.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Metodo SetBrokerNonHAMode Servizi Desktop remoto
- Metodo SetBrokerNonHAMode Servizi Desktop remoto , Win32_SessionBrokerServiceProperties classe
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto, metodo SetBrokerNonHAMode
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
ms.openlocfilehash: 34daa0817056975a6b15164dd29edcbcc86cd7cd9475f753e91500845ce089a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058410"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo SetBrokerNonHAMode della classe \_ SessionBrokerServiceProperties Win32

Esegue la migrazione dei dati dal SQL Server centrale a un database locale. Configura anche il server broker per l'uso del database locale.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connStringToCentralDBRdcms* \[ Pollici\]
</dt> <dd>

Stringa di connessione al database centrale.

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

 

 





