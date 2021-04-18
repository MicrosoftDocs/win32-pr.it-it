---
title: Metodo IsLSinTSLSGroup della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il server licenze Desktop remoto è un membro del gruppo server licenze Desktop remoto in un controller di dominio in un determinato dominio.
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSinTSLSGroup
- Metodo IsLSinTSLSGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSinTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301869"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSinTSLSGroup della \_ classe TSLicenseServer Win32

Recupera un valore che indica se il server licenze Desktop remoto è un membro del gruppo server licenze Desktop remoto in un controller di dominio in un determinato dominio.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Dominio* \[ in\]
</dt> <dd>

Nome del dominio.

</dd> <dt>

*Membro* \[ di out\]
</dt> <dd>

Valore booleano che indica se il server licenze è un membro del gruppo di server licenze Desktop remoto nel dominio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Se non viene specificato alcun nome di dominio, viene eseguita una query su un controller di dominio nello stesso dominio del server licenze.

Il server licenze deve essere membro del gruppo server licenze Desktop remoto se il server è configurato per l'utilizzo dell'ambito di individuazione dominio o foresta. Se il server licenze non è un membro di questo gruppo, il monitoraggio e la creazione di report delle licenze per utente non funzioneranno.

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

[**AddLStoTSLSGroup**](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[**RemoveLSfromTSLSGroup**](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

