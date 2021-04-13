---
title: Metodo UninstallLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Disinstalla un Key Pack per le licenze Servizi Desktop remoto.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UninstallLicenseKeyPack
- Metodo UninstallLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo UninstallLicenseKeyPack
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
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400272"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo UninstallLicenseKeyPack della \_ classe TSLicenseKeyPack Win32

Disinstalla un Key Pack per le licenze Servizi Desktop remoto.

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

*ProductVersion* \[ in\]
</dt> <dd>

Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.

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

Tipo di prodotto del Key Pack di Servizi Desktop remoto License.

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

 

 





