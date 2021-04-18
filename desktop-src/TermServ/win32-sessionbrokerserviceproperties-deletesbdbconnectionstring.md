---
title: Metodo DeleteSBDbConnectionString della classe Win32_SessionBrokerServiceProperties
description: Elimina le stringhe di connessione del database (primaria o secondaria) dal registro di sistema.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteSBDbConnectionString
- Metodo DeleteSBDbConnectionString Servizi Desktop remoto, classe Win32_SessionBrokerServiceProperties
- Classe Win32_SessionBrokerServiceProperties Servizi Desktop remoto, metodo DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301610"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo DeleteSBDbConnectionString della \_ classe SessionBrokerServiceProperties Win32

Elimina le stringhe di connessione del database (primaria o secondaria) dal registro di sistema.

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IsSecondaryConnString* \[ in\]
</dt> <dd>

Se **true**, la stringa di connessione secondaria viene rimossa. Se **false**, la stringa di connessione primaria viene rimossa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                         |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SessionBrokerServiceProperties Win32**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





