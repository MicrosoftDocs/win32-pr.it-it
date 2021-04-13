---
title: Metodo AddLStoTSLSGroup della classe Win32_TSLicenseServer
description: Aggiunge il server licenze Desktop remoto al gruppo server licenze di Connessione Desktop remoto broker (gestore connessione Desktop remoto) in un controller di dominio nello stesso dominio del server licenze Desktop remoto.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddLStoTSLSGroup
- Metodo AddLStoTSLSGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo AddLStoTSLSGroup
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
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400464"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a>Metodo AddLStoTSLSGroup della \_ classe TSLicenseServer Win32

Aggiunge il server licenze Desktop remoto al gruppo server licenze di Connessione Desktop remoto broker (gestore connessione Desktop remoto) in un controller di dominio nello stesso dominio del server licenze Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Domain Admins.

Il server licenze deve essere membro del gruppo server licenze Desktop remoto se il server è configurato per l'utilizzo dell'ambito di individuazione dominio o foresta.

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

[**IsLSinTSLSGroup**](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

