---
title: Metodo RemoveTSCGroup della classe Win32_TSLicenseServer
description: RemoveTSCGroup non è più disponibile per l'uso a Windows Server 2012.
ms.assetid: e5e3eca9-4990-4322-b41d-c6b6b3356272
ms.tgt_platform: multiple
keywords:
- Metodo RemoveTSCGroup Servizi Desktop remoto
- Metodo RemoveTSCGroup Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo RemoveTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebcd3c0eacb54a14675d2794f1c42f8e7a18cd9ea78c7f6369ef883cc3d9fad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127506"
---
# <a name="removetscgroup-method-of-the-win32_tslicenseserver-class"></a>Metodo RemoveTSCGroup della classe \_ Win32 TSLicenseServer

\[**RemoveTSCGroup** non è più disponibile per l'uso a Windows Server 2012.\]

Questo metodo non è supportato.

**Windows Server 2008 R2 e Windows Server 2008:** Rimuove il gruppo locale Computer Terminal Server dal server Desktop remoto licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveTSCGroup();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **WBEM \_ E NOT \_ \_ SUPPORTED**.

**Windows Server 2008 R2 e Windows Server 2008:** Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                                 |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                         |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

