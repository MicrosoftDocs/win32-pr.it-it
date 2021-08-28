---
title: Metodo ReinstallLicenseKeyPackOffline della classe Win32_TSLicenseKeyPack
description: Reinstalla un Servizi Desktop remoto key pack di licenza che usa l'identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Metodo ReinstallLicenseKeyPackOffline Servizi Desktop remoto
- Metodo ReinstallLicenseKeyPackOffline Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , metodo ReinstallLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b72ad2175e0d97cba5733461431726781aebc9a53c1a23f408f7d14e75dd35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058329"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Metodo ReinstallLicenseKeyPackOffline della classe \_ Win32 TSLicenseKeyPack

Reinstalla un Servizi Desktop remoto key pack di licenza che usa l'identificatore di licenza ricevuto tramite Internet o il telefono.

## <a name="syntax"></a>Sintassi


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLicenseKeyPackId* \[ Pollici\]
</dt> <dd>

Contiene il codice di licenza di 35 caratteri. Come input deve essere specificata solo la stringa di caratteri alfanumerici di 35 caratteri. Non è necessario aggiungere trattini.

</dd> <dt>

*KeyPackId* \[ Cambio\]
</dt> <dd>

Riceve l'identificatore del key pack.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





