---
title: Metodo ActivateServerAutomatic della classe Win32_TSLicenseServer
description: Attiva automaticamente il server licenze Desktop remoto tramite Internet.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ActivateServerAutomatic
- Metodo ActivateServerAutomatic Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ActivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963976"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Metodo ActivateServerAutomatic della \_ classe TSLicenseServer Win32

Attiva automaticamente il server licenze Desktop remoto tramite Internet.

## <a name="syntax"></a>Sintassi


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

Lo stato di attivazione restituito può essere uno dei seguenti.

<dt>

0
</dt> <dd>

Il server licenze Desktop remoto viene attivato.

</dd> <dt>

1
</dt> <dd>

Il server licenze Desktop remoto non è attivato.

</dd> <dt>

2
</dt> <dd>

Si è verificato un errore sconosciuto. Non è noto se il server licenze Desktop remoto è attivato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Questo metodo ha esito negativo a meno che non siano impostate le proprietà **FirstName**, **LastName**, **Company** e **CountryRegion** .

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

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

