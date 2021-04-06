---
title: Metodo ReinstallOpenPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Reinstalla un Key Pack per licenze Open License Servizi Desktop remoto.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReinstallOpenPurchaseLicenseKeyPack
- Metodo ReinstallOpenPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ReinstallOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743271"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo ReinstallOpenPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32

Reinstalla un Key Pack per licenze Open License Servizi Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLicenseNumber* \[ in\]
</dt> <dd>

stringa numerica a 8 caratteri fornita con il Key Pack per le licenze. Il parametro *sLicenseNumber* non può contenere trattini.

</dd> <dt>

*sAuthorizationNumber* \[ in\]
</dt> <dd>

stringa alfanumerica a 15 caratteri fornita con il codice di licenza. Il parametro *sAuthorizationNumber* non può contenere trattini.

</dd> <dt>

*ProductVersion* \[ in\]
</dt> <dd>

Versione del prodotto.

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

*ProductType* \[ in\]
</dt> <dd>

Tipo di prodotto.

<dt>

0
</dt> <dd>

Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.

</dd> <dt>

1
</dt> <dd>

Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.

</dd> <dt>

2
</dt> <dd>

Questo tipo di prodotto non è valido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ in\]
</dt> <dd>

Numero di licenze da installare.

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

 

 





