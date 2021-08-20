---
title: Metodo SetSBDbConnectionStrings della classe Win32_SessionBrokerServiceProperties
description: Salva le stringhe di connessione del database, sia primari che secondarie, nel Registro di sistema.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Metodo SetSBDbConnectionStrings Servizi Desktop remoto
- Metodo SetSBDbConnectionStrings Servizi Desktop remoto , Win32_SessionBrokerServiceProperties classe
- Win32_SessionBrokerServiceProperties classe Servizi Desktop remoto , metodo SetSBDbConnectionStrings
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b89baa40d25e6ecf316ac6904cc89091fa581d87be1018c52fa31c2b7ab358d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058418"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Metodo SetSBDbConnectionStrings della classe \_ SessionBrokerServiceProperties Win32

Salva le stringhe di connessione del database, sia primari che secondarie, nel Registro di sistema.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connStringToCentralDBRdcms* \[ Pollici\]
</dt> <dd>

Stringa di connessione primaria.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ Pollici\]
</dt> <dd>

Stringa di connessione secondaria.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                         |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





