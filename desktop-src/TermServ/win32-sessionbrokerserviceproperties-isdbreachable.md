---
title: Metodo IsDbReachable della classe Win32_SessionBrokerServiceProperties
description: Controlla se il database è raggiungibile.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsDbReachable
- Metodo IsDbReachable Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476690"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo IsDbReachable della \_ classe SessionBrokerServiceProperties Win32

Controlla se il database è raggiungibile.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connStringToDb* \[ in\]
</dt> <dd>

Stringa di connessione al database.

</dd> <dt>

*connSecondaryStringToDb* \[ in\]
</dt> <dd>

Stringa di connessione secondaria al database centrale.

**Windows server 2012 R2 e Windows server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.

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

 

 





