---
title: Metodo IsDbReachable della classe Win32_SessionBrokerServiceProperties
description: Verifica se il database è raggiungibile.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Metodo IsDbReachable Servizi Desktop remoto
- Metodo IsDbReachable Servizi Desktop remoto , Win32_SessionBrokerServiceProperties classe
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto metodo , IsDbReachable
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
ms.openlocfilehash: c1cd7aaf2035251c503d85683f9aa9e9fe7b7f6285084a97133f0573ba41d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848418"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo IsDbReachable della classe \_ SessionBrokerServiceProperties Win32

Verifica se il database è raggiungibile.

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

*connStringToDb* \[ Pollici\]
</dt> <dd>

Stringa di connessione al database.

</dd> <dt>

*connSecondaryStringToDb* \[ Pollici\]
</dt> <dd>

Stringa di connessione secondaria al database centrale.

**Windows Server 2012 R2 e Windows Server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.

</dd> <dt>

*activeBrokerName* \[ Pollici\]
</dt> <dd>

Nome del broker attivo.

**Windows Server 2012 R2 e Windows Server 2012:** Questo parametro non è disponibile prima di Windows Server 2016.

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

 

 





