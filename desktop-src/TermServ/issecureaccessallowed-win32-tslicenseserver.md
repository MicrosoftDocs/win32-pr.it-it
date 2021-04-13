---
title: Metodo IsSecureAccessAllowed della classe Win32_TSLicenseServer
description: Recupera un valore che indica se host sessione Desktop remoto un server Host sessione Desktop remoto può richiedere Servizi Desktop remoto licenze di accesso client (RDS \ 160; Licenze CAL) dal server licenze Desktop remoto.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsSecureAccessAllowed
- Metodo IsSecureAccessAllowed Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsSecureAccessAllowed
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsSecureAccessAllowed
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf35fd8b38139027955fde51a209000435744f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517740"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Metodo IsSecureAccessAllowed della \_ classe TSLicenseServer Win32

Recupera un valore che indica se un server Host sessione Desktop remoto (host sessione Desktop remoto) può richiedere Servizi Desktop remoto licenze CAL (Client Access License) dal server licenze Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tsname* \[ in\]
</dt> <dd>

Nome del server Host sessione Desktop remoto.

</dd> <dt>

*Consentito* \[ out\]
</dt> <dd>

Valore booleano che indica se il server Host sessione Desktop remoto è autorizzato a richiedere licenze CAL Servizi Desktop remoto dal server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Il valore restituito è basato sull'impostazione di criteri di gruppo "gruppo di sicurezza del server licenze" e sull'appartenenza al gruppo locale computer Terminal Server nel server licenze Desktop remoto.

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
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

