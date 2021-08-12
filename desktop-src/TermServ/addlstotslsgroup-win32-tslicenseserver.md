---
title: Metodo AddLStoTSLSGroup della classe Win32_TSLicenseServer
description: Aggiunge il server Desktop remoto licenze al gruppo server licenze di Connessione Desktop remoto Broker (Gestore connessione Desktop remoto) in un controller di dominio nello stesso dominio del server licenze Desktop remoto server licenze.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Metodo AddLStoTSLSGroup Servizi Desktop remoto
- Metodo AddLStoTSLSGroup Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf3d0464b42159ca1827caf579e21982c08d066495cd664ec1adfcaa883a4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610406"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>Metodo AddLStoTSLSGroup della classe \_ TSLicenseServer Win32

Aggiunge il server Desktop remoto licenze al gruppo server licenze di Connessione Desktop remoto Broker (Gestore connessione Desktop remoto) in un controller di dominio nello stesso dominio del server licenze Desktop remoto server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Domain Admins.

Il server licenze deve essere membro del gruppo Desktop remoto server licenze se il server è configurato per l'utilizzo dell'ambito di individuazione del dominio o della foresta.

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

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

