---
title: Metodo IsLSRegisteredToSCP della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.
ms.assetid: 013C3711-7C55-4DB4-9229-C3C60E751EF2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSRegisteredToSCP
- Metodo IsLSRegisteredToSCP Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSRegisteredToSCP
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSRegisteredToSCP
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b203ff580c5ff8871d023c7f349626acdd693f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740186"
---
# <a name="islsregisteredtoscp-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSRegisteredToSCP della \_ classe TSLicenseServer Win32

Recupera un valore che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSRegisteredToSCP(
  [out] boolean Registered
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Registrato* \[ out\]
</dt> <dd>

Valore booleano che indica se il server licenze Desktop remoto viene registrato come punto di connessione del servizio nel Active Directory Domain Services.

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
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                         |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

