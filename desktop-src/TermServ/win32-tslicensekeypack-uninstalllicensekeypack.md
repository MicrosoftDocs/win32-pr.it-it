---
title: Metodo UninstallLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Disinstalla un key pack Servizi Desktop remoto licenza.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Metodo UninstallLicenseKeyPack Servizi Desktop remoto
- Metodo UninstallLicenseKeyPack Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto, metodo UninstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb02ff8ecc84c346bef404071e8abb3988c0e7c8e70b54b288524e8ef790d5fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348622"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo UninstallLicenseKeyPack della classe \_ Win32 TSLicenseKeyPack

Disinstalla un key pack Servizi Desktop remoto licenza.

## <a name="syntax"></a>Sintassi


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ProductVersion* \[ Pollici\]
</dt> <dd>

Identificatore della versione del prodotto per il key pack Servizi Desktop remoto licenza.

<dt>

0
</dt> <dd>

Non supportata.

</dd> <dt>

1
</dt> <dd>

Non supportata.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ Pollici\]
</dt> <dd>

Tipo di prodotto del key pack Servizi Desktop remoto licenza.

<dt>

0
</dt> <dd>

Il Servizi Desktop remoto prodotto key pack di licenza è per dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve avere una licenza.

</dd> <dt>

1
</dt> <dd>

Il Servizi Desktop remoto prodotto key pack di licenza è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve avere una licenza.

</dd> <dt>

2
</dt> <dd>

Questo tipo di prodotto non è valido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ Pollici\]
</dt> <dd>

Numero di licenze da disinstallare.

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

 

 





