---
title: Metodo IsTSCGroupPresent della Win32_TSLicenseServer classe
description: IsTSCGroupPresent non è più disponibile per l'uso a Windows Server 2012.
ms.assetid: 2bbb00ff-4fb3-4a7a-a0e7-3daabf97d70a
ms.tgt_platform: multiple
keywords:
- Metodo IsTSCGroupPresent Servizi Desktop remoto
- Metodo IsTSCGroupPresent Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo IsTSCGroupPresent
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsTSCGroupPresent
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4711236541999264a5a6f96066050f709cdcc087a751e0e56ddd6dea1b9103da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351340"
---
# <a name="istscgrouppresent-method-of-the-win32_tslicenseserver-class"></a>Metodo IsTSCGroupPresent della classe \_ Win32 TSLicenseServer

\[**IsTSCGroupPresent** non è più disponibile per l'uso a Windows Server 2012.\]

Questo metodo non è supportato.

**Windows Server 2008 R2 e Windows Server 2008:** Recupera un valore che indica se il gruppo locale Computer Terminal Server esiste nel server Desktop remoto licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsTSCGroupPresent(
  [out] boolean Present
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Presente* \[ Cambio\]
</dt> <dd>

Valore booleano che indica se il gruppo locale Computer Terminal Server esiste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **WBEM \_ E NON \_ \_ SUPPORTATO.**

**Windows Server 2008 R2 e Windows Server 2008:** Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> </dl>

 

