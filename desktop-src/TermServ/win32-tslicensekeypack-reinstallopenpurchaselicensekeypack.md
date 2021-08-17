---
title: Metodo ReinstallOpenPurchaseLicenseKeyPack Win32_TSLicenseKeyPack classe
description: Reinstalla un Key Pack Servizi Desktop remoto licenza Open License.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Metodo ReinstallOpenPurchaseLicenseKeyPack Servizi Desktop remoto
- Metodo ReinstallOpenPurchaseLicenseKeyPack Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , metodo ReinstallOpenPurchaseLicenseKeyPack
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
ms.openlocfilehash: 6519e6eedc187b6db2ee93a776843b0f305430df7ae55e4356ebce4de5ad31d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137824"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo ReinstallOpenPurchaseLicenseKeyPack della classe \_ Win32 TSLicenseKeyPack

Reinstalla un Key Pack Servizi Desktop remoto licenza Open License.

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

*sLicenseNumber* \[ Pollici\]
</dt> <dd>

Stringa numerica di 8 caratteri fornita con il key pack di licenza. Il *parametro sLicenseNumber* non può contenere trattini.

</dd> <dt>

*sAuthorizationNumber* \[ Pollici\]
</dt> <dd>

Stringa alfanumerica di 15 caratteri fornita con il codice di licenza. Il *parametro sAuthorizationNumber* non può contenere trattini.

</dd> <dt>

*ProductVersion* \[ Pollici\]
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

*ProductType* \[ Pollici\]
</dt> <dd>

Tipo di prodotto.

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

Numero di licenze da installare.

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

 

 





