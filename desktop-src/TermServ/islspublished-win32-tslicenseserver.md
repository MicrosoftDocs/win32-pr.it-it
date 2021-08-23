---
title: Metodo IsLSPublished della classe Win32_TSLicenseServer
description: Recupera un valore che Desktop remoto server licenze è pubblicato in Active Directory Domain Services (AD \ 160;DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Metodo IsLSPublished Servizi Desktop remoto
- Metodo IsLSPublished Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo IsLSPublished
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a5ca1fd4159b5b632dde5930f25b28ccbc7fcbad41ee2ee2da126252c6eb086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000651"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSPublished della classe \_ Win32 TSLicenseServer

Recupera un valore che indica se Desktop remoto server licenze è pubblicato in Active Directory Domain Services (AD DS).

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pubblicato* \[ Cambio\]
</dt> <dd>

Valore booleano che indica se il server licenze è pubblicato in Servizi di dominio Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Se il server licenze viene pubblicato in Servizi di dominio Active Directory, sarà automaticamente individuabile dai server host sessione Desktop remoto (Host sessione Desktop remoto) nella stessa foresta.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> </dl>

 

