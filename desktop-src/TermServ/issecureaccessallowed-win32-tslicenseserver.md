---
title: Metodo IsSecureAccessAllowed della classe Win32_TSLicenseServer
description: Recupera un valore che indica se Desktop remoto un server host sessione Desktop remoto è autorizzato a richiedere Servizi Desktop remoto licenze di accesso client (Servizi Desktop remoto \ 160; licenze CAL) dal server Desktop remoto licenze.
ms.assetid: b9124808-79be-4b94-b12b-f093d5e8195a
ms.tgt_platform: multiple
keywords:
- Metodo IsSecureAccessAllowed Servizi Desktop remoto
- Metodo IsSecureAccessAllowed Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto metodo , IsSecureAccessAllowed
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
ms.openlocfilehash: 6109eb363459432d50d54eb8521f0f23bb54a0836c82f92af20a5b83b64f1d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351363"
---
# <a name="issecureaccessallowed-method-of-the-win32_tslicenseserver-class"></a>Metodo IsSecureAccessAllowed della classe \_ TSLicenseServer Win32

Recupera Desktop remoto un valore che indica se a un server host sessione Desktop remoto è consentito richiedere Servizi Desktop remoto licenze CAL (Client Access License) dal server licenze Desktop remoto servizi Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsSecureAccessAllowed(
  [in]  string  tsname,
  [out] boolean Allowed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tsname* \[ Pollici\]
</dt> <dd>

Nome del server Host sessione Desktop remoto.

</dd> <dt>

*Consentito* \[ Cambio\]
</dt> <dd>

Valore booleano che indica se al server Host sessione Desktop remoto è consentito richiedere licenze CAL Servizi Desktop remoto dal server licenze.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Il valore restituito si basa sull'impostazione dei criteri di gruppo "gruppo di sicurezza del server licenze" e sull'appartenenza al gruppo locale Computer Terminal Server Desktop remoto server licenze.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsLSSecGrpGPEnabled**](islssecgrpgpenabled-win32-tslicenseserver.md)
</dt> </dl>

 

