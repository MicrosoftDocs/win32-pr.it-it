---
title: Metodo GetInt32Property della classe Win32_RDMSDeploymentSettings (Microsoft.diagnostics.appanalysis.h)
description: Recupera una proprietà integer per le impostazioni di distribuzione di una raccolta di desktop virtuali.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- Metodo GetInt32Property Servizi Desktop remoto
- Metodo GetInt32Property Servizi Desktop remoto , Win32_RDMSDeploymentSettings classe
- Win32_RDMSDeploymentSettings classe Servizi Desktop remoto metodo , GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac79fdacf6b8f64d354158f964be1019692933a10409a8bf085109d9f5a9a31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130760"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Metodo GetInt32Property della classe \_ RDMSDeploymentSettings Win32

Recupera una proprietà integer per le impostazioni di distribuzione di una raccolta di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Alias della raccolta di desktop virtuali.

</dd> <dt>

*Valore* \[ Cambio\]
</dt> <dd>

Intero che riceve il valore recuperato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                 |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSDeploymentSettings**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





