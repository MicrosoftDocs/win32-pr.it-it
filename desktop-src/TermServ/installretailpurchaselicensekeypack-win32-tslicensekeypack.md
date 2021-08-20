---
title: Metodo InstallRetailPurchaseLicenseKeyPack Win32_TSLicenseKeyPack classe
description: Installa un key pack Servizi Desktop remoto licenza acquistato tramite un canale di vendita al dettaglio.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- Metodo InstallRetailPurchaseLicenseKeyPack Servizi Desktop remoto
- Metodo InstallRetailPurchaseLicenseKeyPack Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto, metodo InstallRetailPurchaseLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427107e6d581c839ee83767c7c95426e13d16a392b7764924997c01785b85d46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129592"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo InstallRetailPurchaseLicenseKeyPack della classe \_ Win32 TSLicenseKeyPack

Installa un key pack Servizi Desktop remoto licenza acquistato tramite un canale di vendita al dettaglio.

## <a name="syntax"></a>Sintassi


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLicenseCode* \[ Pollici\]
</dt> <dd>

Contiene il codice di licenza di 25 caratteri. Come input deve essere specificata solo la stringa di caratteri alfanumerici di 25 caratteri. Non è necessario aggiungere trattini.

</dd> <dt>

*KeyPackId* \[ Cambio\]
</dt> <dd>

Riceve l'identificatore del key pack.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

