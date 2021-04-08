---
title: Metodo RemoveLicensesWithIdCount della classe Win32_TSLicenseKeyPack
description: Rimuove il numero specificato di Servizi Desktop remoto licenze dal Key Pack specificato.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveLicensesWithIdCount
- Metodo RemoveLicensesWithIdCount Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo RemoveLicensesWithIdCount
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047954"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a>Metodo RemoveLicensesWithIdCount della \_ classe TSLicenseKeyPack Win32

Rimuove il numero specificato di Servizi Desktop remoto licenze dal Key Pack specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*KeyPackId* \[ in\]
</dt> <dd>

Identificatore del Key Pack che contiene le licenze da rimuovere.

</dd> <dt>

*LicenseCount* \[ in\]
</dt> <dd>

Numero di licenze da disinstallare.

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

 

 





