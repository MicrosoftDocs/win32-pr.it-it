---
title: Metodo Create della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Crea un criterio di autorizzazione risorse Desktop remoto (RD \ 160; RAP).
ms.assetid: 3301a543-cdf9-4528-a29e-691054ef81c9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto crea metodo
- Create Method Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo create
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6372706a294902b03f22807049db9a954de4f7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400334"
---
# <a name="create-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a>Metodo Create della classe Win32 \_ TSGatewayResourceAuthorizationPolicy

Crea un criterio di autorizzazione risorse Desktop remoto (RD RAP).

## <a name="syntax"></a>Sintassi


```mof
uint32 Create(
  [in] string  Name,
  [in] string  Description,
  [in] boolean Enabled,
  [in] string  ResourceGroupType,
  [in] string  ResourceGroupName,
  [in] string  UserGroupNames,
  [in] string  ProtocolNames,
  [in] string  PortNumbers
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome dei criteri di autorizzazione connessioni Desktop remoto.

</dd> <dt>

*Descrizione* \[ di in\]
</dt> <dd>

Descrizione del criterio di autorizzazione connessioni Desktop remoto.

</dd> <dt>

*Abilitato* \[ in\]
</dt> <dd>

Indica se è necessario abilitare RD RAP.

</dd> <dt>

*ResourceGroupType* \[ in\]
</dt> <dd>

Tipo di gruppo di risorse.

<dt>

RG
</dt> <dd>

Gruppo di risorse.

</dd> <dt>

CG
</dt> <dd>

Gruppo di computer, come Archiviato in Active Directory Domain Services.

</dd> <dt>

TUTTI
</dt> <dd>

Tutte le risorse.

</dd> </dl> </dd> <dt>

*ResourceGroupName* \[ in\]
</dt> <dd>

Nome del gruppo di risorse.

</dd> <dt>

*UserGroupNames* \[ in\]
</dt> <dd>

Elenco delimitato da punti e virgola di nomi di gruppi di utenti. Se l'utente appartiene a uno di questi gruppi di utenti, sarà consentito l'accesso. I nomi dei gruppi di utenti devono essere nel formato *dominio \\ nomegruppoutenti*.

</dd> <dt>

*ProtocolNames* \[ in\]
</dt> <dd>

Elenco delimitato da punti e virgola di nomi di protocollo abilitati per questo criterio. I nomi devono corrispondere alla restituzione del metodo [**Getprotocolname**](getprotocolname-win32-tsgatewayserversettings.md) della [**classe \_ Win32 TSGatewayServerSettings**](win32-tsgatewayserversettings.md) .

</dd> <dt>

*PortNumbers* \[ in\]
</dt> <dd>

Elenco delimitato da punti e virgola di numeri di porta abilitati per questo criterio. Per consentire qualsiasi numero di porta, impostare " \* ".

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

