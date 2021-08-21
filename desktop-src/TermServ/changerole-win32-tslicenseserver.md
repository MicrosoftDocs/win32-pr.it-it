---
title: Metodo ChangeRole della classe Win32_TSLicenseServer
description: Modifica l'ambito di individuazione del Desktop remoto licenze. L'ambito di individuazione determina Desktop remoto server Host sessione Desktop remoto nella rete in grado di individuare automaticamente il server licenze.
ms.assetid: 3d98fd8a-4ade-489f-8edd-5df1227f15cd
ms.tgt_platform: multiple
keywords:
- Metodo ChangeRole Servizi Desktop remoto
- Metodo ChangeRole Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo ChangeRole
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ChangeRole
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f010fc1c8d31382040d79bd811e4a472af4269d503d2810e44320717ebbc5e35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575081"
---
# <a name="changerole-method-of-the-win32_tslicenseserver-class"></a>Metodo ChangeRole della classe \_ TSLicenseServer Win32

Modifica l'ambito di individuazione del Desktop remoto licenze. L'ambito di individuazione determina Desktop remoto server Host sessione Desktop remoto nella rete in grado di individuare automaticamente il server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeRole(
  [in] uint32 ServerRole
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ServerRole* \[ Pollici\]
</dt> <dd>

Ambito di individuazione per il Desktop remoto licenze. È possibile impostare uno dei valori seguenti.

<dt>

0
</dt> <dd>

I server Host sessione Desktop remoto nello stesso gruppo di lavoro possono individuare il server licenze.

</dd> <dt>

1
</dt> <dd>

I server Host sessione Desktop remoto nello stesso dominio possono individuare il server licenze. Per impostare questo valore, è necessario essere connessi come amministratore di dominio.

</dd> <dt>

2
</dt> <dd>

I server Host sessione Desktop remoto da più domini nella stessa foresta possono individuare il server licenze. Per impostare questo valore, è necessario essere connessi come amministratore dell'organizzazione.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

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
</dt> </dl>

 

