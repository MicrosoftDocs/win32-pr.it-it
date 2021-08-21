---
title: Metodo ImportOpenPurchaseLicenseKeyPack della Win32_TSLicenseKeyPack classe
description: Importa, da un altro server Desktop remoto licenze, un key pack open license Servizi Desktop remoto licenza.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Metodo ImportOpenPurchaseLicenseKeyPack Servizi Desktop remoto
- Metodo ImportOpenPurchaseLicenseKeyPack Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , metodo ImportOpenPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 768961bda04776a73d0aa74422ce0ed5088e041ee41e4732becd72914dcabf04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008471"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo ImportOpenPurchaseLicenseKeyPack della classe \_ Win32 TSLicenseKeyPack

Importa, da un altro server Desktop remoto licenze, un key pack open license Servizi Desktop remoto licenza.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
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

Il Servizi Desktop remoto di prodotto del key pack di licenza è per ogni dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve avere una licenza.

</dd> <dt>

1
</dt> <dd>

Il Servizi Desktop remoto del prodotto key pack di licenza è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve avere una licenza.

</dd> <dt>

2
</dt> <dd>

Questo tipo di prodotto non è valido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ Pollici\]
</dt> <dd>

Numero di licenze da importare

</dd> <dt>

*sSourceLSName* \[ Pollici\]
</dt> <dd>

Nome del server licenze Desktop remoto di origine. Si tratta del nome distinto completo o dell'indirizzo IP del server.

</dd> <dt>

*sSourceLSProductId* \[ Pollici\]
</dt> <dd>

Identificatore Desktop remoto server licenze. è una stringa alfanumerica di 35 caratteri che non può includere trattini.

</dd> <dt>

*KeyPackId* \[ Cambio\]
</dt> <dd>

Riceve l'identificatore del key pack.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

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

 

 





