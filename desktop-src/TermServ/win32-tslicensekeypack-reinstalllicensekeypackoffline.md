---
title: Metodo ReinstallLicenseKeyPackOffline della classe Win32_TSLicenseKeyPack
description: Reinstalla un Key Pack di Servizi Desktop remoto License che utilizza l'identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReinstallLicenseKeyPackOffline
- Metodo ReinstallLicenseKeyPackOffline Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ReinstallLicenseKeyPackOffline
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
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873409"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Metodo ReinstallLicenseKeyPackOffline della \_ classe TSLicenseKeyPack Win32

Reinstalla un Key Pack di Servizi Desktop remoto License che utilizza l'identificatore di licenza ricevuto tramite Internet o il telefono.

## <a name="syntax"></a>Sintassi


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLicenseKeyPackId* \[ in\]
</dt> <dd>

Contiene il codice di licenza a 35 caratteri. Come input è necessario assegnare solo la stringa di caratteri alfanumerici a 35 caratteri. Nessun trattino da aggiungere.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Riceve l'identificatore del Key Pack.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





