---
title: Metodo Import della classe Win32_TSGatewayServer
description: Importa una determinata configurazione nel server Desktop remoto Gateway Desktop remoto.
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Metodo Import Servizi Desktop remoto
- Metodo Import Servizi Desktop remoto , Win32_TSGatewayServer classe
- Win32_TSGatewayServer classe Servizi Desktop remoto , metodo Import
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Import
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2629e8e44acd0f617e86a846cc127ab77250673c8612f2d2f53ab8c0238d9f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574571"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Metodo Import della classe \_ TSGatewayServer Win32

Importa una determinata configurazione nel server Desktop remoto Gateway Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 Import(
  [in]  uint32 ImportType,
  [in]  string XmlString,
  [in]  uint32 MergeOrReplace,
  [out] string LogString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ImportType* \[ Pollici\]
</dt> <dd>

Contenuto da importare. Impostare il tipo di importazione impostando i bit corrispondenti nel *parametro ImportType.* È possibile impostare più tipi di importazione. Ad esempio, se è impostato il bit 0, Servizi Desktop remoto criteri di autorizzazione connessione Desktop remoto verranno importati. Se è impostato sia il bit 0 che il secondo bit, verranno importati sia i criteri di autorizzazione delle risorse di Servizi Desktop remoto desktop remoto sia i criteri di autorizzazione risorse di rete.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importare tutti i CAP** (1)


</dt> <dd>

Importare tutti i CAP di Desktop remoto.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importare tutti i server Radius** (2)


</dt> <dd>

Importare un elenco di tutti i server del server dei criteri di rete( NPS).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importare tutti i file RAP** (4)


</dt> <dd>

Importare tutti i criteri di autorizzazione connessioni Desktop remoto.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importare tutti i RG** (8)


</dt> <dd>

Importare tutti i gruppi di risorse.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importare tutti i server LoadBalancing** (16)


</dt> <dd>

Importare un elenco di tutti i server di bilanciamento del carico.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importare tutti i Impostazioni** server (32)


</dt> <dd>

Importare tutte le impostazioni del server correlate a Gateway Desktop remoto.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importare tutti i criteri di integrità** (64)


</dt> <dd>

Importare tutti i criteri di integrità.

**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: **

Questo valore non è supportato prima di Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ Pollici\]
</dt> <dd>

Configurazione come stringa XML.

</dd> <dt>

*MergeOrReplace* \[ Pollici\]
</dt> <dd>

Indica se unire o sostituire i dati quando si verifica un conflitto.

> [!Note]  
> L'unione non è ancora implementata. Di conseguenza, questo valore del parametro viene ignorato.

 

</dd> <dt>

*LogString* \[ Cambio\]
</dt> <dd>

Informazioni del log generate durante l'operazione di importazione.

</dd> </dl>

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

[**Win32 \_ TSGatewayServer**](win32-tsgatewayserver.md)
</dt> </dl>

 

