---
title: Metodo CreateTSCGroup della Win32_TSLicenseServer classe
description: CreateTSCGroup non è più disponibile per l'uso a Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Metodo CreateTSCGroup Servizi Desktop remoto
- Metodo CreateTSCGroup Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo CreateTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf363d86cf663a3f9b626d9586140eb4c00f86e9750070f8a2000149b655bb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737871"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a>Metodo CreateTSCGroup della classe \_ Win32 TSLicenseServer

\[**CreateTSCGroup** non è più disponibile per l'uso a Windows Server 2012.\]

Questo metodo non è supportato.

**Windows Server 2008 R2 e Windows Server 2008:** Crea il gruppo locale Computer Terminal Server nel server Desktop remoto licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **WBEM \_ E NON \_ \_ SUPPORTATO.**

**Windows Server 2008 R2 e Windows Server 2008:** Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

