---
title: Metodo InstallLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Installa un Key Pack per le licenze Servizi Desktop remoto che usa l'identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: 1e545186-cc01-4700-857f-9390e1b73923
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallLicenseKeyPack
- Metodo InstallLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo InstallLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bee5e03de19783a20eeafa3f652dd60b99e871c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963903"
---
# <a name="installlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo InstallLicenseKeyPack della \_ classe TSLicenseKeyPack Win32

Installa un Key Pack per le licenze Servizi Desktop remoto che usa l'identificatore di licenza ricevuto tramite Internet o il telefono.

## <a name="syntax"></a>Sintassi


```mof
uint32 InstallLicenseKeyPack(
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

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

