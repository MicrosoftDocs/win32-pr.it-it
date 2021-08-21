---
title: Metodo SetBrokerHAMode della Win32_SessionBrokerServiceProperties classe
description: Esegue la migrazione dei dati da un database WID locale al nuovo database SQL database basato su server. Configura inoltre il server broker per l'uso del server SQL centrale.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Metodo SetBrokerHAMode Servizi Desktop remoto
- Metodo SetBrokerHAMode Servizi Desktop remoto , Win32_SessionBrokerServiceProperties classe
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto, metodo SetBrokerHAMode
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
ms.openlocfilehash: 17b72233b51686911e4b1d0a661f4e46fa9bcaa813bb6ccc973b2f8a5b12da24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604550"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo SetBrokerHAMode della classe \_ SessionBrokerServiceProperties Win32

Esegue la migrazione dei dati da un database WID locale al nuovo database SQL database basato su server. Configura inoltre il server broker per l'uso del server SQL centrale.

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

*connStringToCentralDBRdcms* \[ Pollici\]
</dt> <dd>

Stringa di connessione al database centrale.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ Pollici\]
</dt> <dd>

Stringa di connessione secondaria al database centrale.

**Windows Server 2012 R2 e Windows Server 2012:** Questo parametro non è disponibile prima Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ Pollici\]
</dt> <dd>

Nome DNS broker.

</dd> <dt>

*activeBrokerName* \[ Pollici\]
</dt> <dd>

Nome broker attivo.

**Windows Server 2012 R2 e Windows Server 2012:** Questo parametro non è disponibile prima Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà \_ sessionBrokerServiceProperties win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





