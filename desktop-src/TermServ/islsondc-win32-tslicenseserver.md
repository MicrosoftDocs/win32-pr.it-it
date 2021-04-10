---
title: Metodo IsLSonDC della classe Win32_TSLicenseServer
description: Recupera un valore che indica se in un controller di dominio è installato Desktop remoto Licensing (licenze Desktop remoto).
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSonDC
- Metodo IsLSonDC Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSonDC
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ddbf01615903150ffa8f97fca88cfcf7fda937
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964418"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSonDC della \_ classe TSLicenseServer Win32

Recupera un valore che indica se in un controller di dominio è installato Desktop remoto Licensing (licenze Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OnDC* \[ out\]
</dt> <dd>

Valore booleano che indica se il servizio licenze Desktop remoto è installato in un controller di dominio.

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

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

