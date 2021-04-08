---
title: Metodo ImportRetailPurchaseLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportRetailPurchaseLicenseKeyPack
- Metodo ImportRetailPurchaseLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741767"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo ImportRetailPurchaseLicenseKeyPack della \_ classe TSLicenseKeyPack Win32

Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLicenseCode* \[ in\]
</dt> <dd>

Contiene il codice di licenza di 25 caratteri. Come input deve essere specificata solo la stringa di caratteri alfanumerici di 25 caratteri. Nessun trattino da aggiungere.

</dd> <dt>

*sSourceLSName* \[ in\]
</dt> <dd>

Nome dell'origine Desktop remoto server licenze. Si tratta del nome distinto completo o dell'indirizzo IP del server.

</dd> <dt>

*sSourceLSProductId* \[ in\]
</dt> <dd>

Identificatore del server licenze Desktop remoto. È una stringa alfanumerica di 35 caratteri che non può includere trattini.

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

 

 





