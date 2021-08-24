---
title: Metodo Update della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Aggiorna i criteri di Desktop remoto risorse correnti (RD \ 160; RAP).
ms.assetid: af997bb8-6027-4f37-80fb-e89622840a2b
ms.tgt_platform: multiple
keywords:
- Aggiornare il metodo Servizi Desktop remoto
- Metodo Update Servizi Desktop remoto , Win32_TSGatewayResourceAuthorizationPolicy classe
- Win32_TSGatewayResourceAuthorizationPolicy classe Servizi Desktop remoto , metodo Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330bf14759f7cdef129a4c34b32acde1d610619c7f54f7d6ec95789e6bec390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868921"
---
# <a name="update-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo Update della classe \_ TSGatewayResourceAuthorizationPolicy Win32

Aggiorna i criteri di autorizzazione Desktop remoto risorse correnti .

## <a name="syntax"></a>Sintassi


```mof
uint32 Update(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupName,
  [in] string  ResourceGroupType,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Nome dell'istanza di Criteri di gruppo di Desktop remoto.

</dd> <dt>

*Descrizione* \[ Pollici\]
</dt> <dd>

Descrizione di RD RAP.

</dd> <dt>

*Abilitato* \[ Pollici\]
</dt> <dd>

Indica se l'applicazione di criteri di protezione desktop remoto deve essere abilitata.

</dd> <dt>

*ResourceGroupName* \[ Pollici\]
</dt> <dd>

Nome del gruppo di risorse associato a questo GRUPPO DI RISORSE DESKTOP REMOTO.

</dd> <dt>

*ResourceGroupType* \[ Pollici\]
</dt> <dd>

Tipo di gruppo di risorse.

<dt>

"RG"
</dt> <dd>

Gruppo di risorse.

</dd> <dt>

"CG"
</dt> <dd>

Gruppo di computer, come archiviato in Active Directory Domain Services.

</dd> <dt>

"ALL"
</dt> <dd>

Tutte le risorse.

</dd> </dl> </dd> <dt>

*UserGroupNames* \[ Pollici\]
</dt> <dd>

Elenco di nomi di gruppi di utenti separati da punto e virgola. I nomi sono nel formato *Dominio \\ NomeGruppoUtente*. Se l'utente appartiene a uno di questi gruppi di utenti, l'accesso sarà consentito.

</dd> <dt>

*ProtocolNames* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punto e virgola dei nomi di protocollo abilitati per questo criterio. I nomi devono corrispondere alla restituzione [**del metodo GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md) della [**classe Win32 \_ TSGatewayServerSettings.**](win32-tsgatewayserversettings.md)

</dd> <dt>

*Numeroporta* \[ Pollici\]
</dt> <dd>

Elenco delimitato da punto e virgola dei numeri di porta abilitati per questo criterio. Per consentire qualsiasi numero di porta, impostare " \* ".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

