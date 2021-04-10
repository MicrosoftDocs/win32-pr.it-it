---
title: Metodo di importazione della classe Win32_TSGatewayServer
description: Importa una determinata configurazione nel server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: d849afb9-f6cb-41e6-aab5-e47b30a5581f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di importazione
- Servizi Desktop remoto metodo di importazione, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Servizi Desktop remoto, metodo Import
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
ms.openlocfilehash: 9b35395342be7c13f2a96f73f914eda103e1ef4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964430"
---
# <a name="import-method-of-the-win32_tsgatewayserver-class"></a>Metodo Import della classe Win32 \_ TSGatewayServer

Importa una determinata configurazione nel server Gateway Desktop remoto (Gateway Desktop remoto).

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

*ImportType* \[ in\]
</dt> <dd>

Contenuto da importare. Impostare il tipo di importazione impostando i bit corrispondenti nel parametro *ImportType* . È possibile impostare più tipi di importazione. Se, ad esempio, è impostato il bit 0, verranno importati Servizi Desktop remoto i criteri di autorizzazione della connessione. Se è impostato sia il bit 0 che il secondo bit, verranno importati sia i criteri di autorizzazione connessioni Desktop remoto che i criteri di autorizzazione risorse Servizi Desktop remoto.

<dt>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>

<span id="Import_all_CAPs"></span><span id="import_all_caps"></span><span id="IMPORT_ALL_CAPS"></span>**Importa tutti i Caps** (1)


</dt> <dd>

Importa tutti i tappi desktop remoto.

</dd> <dt>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>

<span id="Import_all_Radius_Servers"></span><span id="import_all_radius_servers"></span><span id="IMPORT_ALL_RADIUS_SERVERS"></span>**Importa tutti i server RADIUS** (2)


</dt> <dd>

Importare un elenco di tutti i server dei criteri di rete (NPS).

</dd> <dt>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>

<span id="Import_all_RAPs"></span><span id="import_all_raps"></span><span id="IMPORT_ALL_RAPS"></span>**Importa tutti i rap** (4)


</dt> <dd>

Importa tutti i rap RD.

</dd> <dt>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>

<span id="Import_all_RGs"></span><span id="import_all_rgs"></span><span id="IMPORT_ALL_RGS"></span>**Importa tutti i RGS** (8)


</dt> <dd>

Importare tutti i gruppi di risorse.

</dd> <dt>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Import_all_LoadBalancing_Servers"></span><span id="import_all_loadbalancing_servers"></span><span id="IMPORT_ALL_LOADBALANCING_SERVERS"></span>**Importa tutti i Server Loadbalancing** (16)


</dt> <dd>

Importare un elenco di tutti i server di bilanciamento del carico.

</dd> <dt>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>

<span id="Import_all_Server_Settings"></span><span id="import_all_server_settings"></span><span id="IMPORT_ALL_SERVER_SETTINGS"></span>**Importa tutte le impostazioni del server** (32)


</dt> <dd>

Importa tutte le impostazioni del server correlate a Gateway Desktop remoto.

</dd> <dt>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>

<span id="Import_all_Health_Policies"></span><span id="import_all_health_policies"></span><span id="IMPORT_ALL_HEALTH_POLICIES"></span>**Importa tutti i criteri di integrità** (64)


</dt> <dd>

Importa tutti i criteri di integrità.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: * *

Questo valore non è supportato prima di Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ in\]
</dt> <dd>

Configurazione come stringa XML.

</dd> <dt>

*MergeOrReplace* \[ in\]
</dt> <dd>

Indica se unire o sostituire i dati quando si verifica un conflitto.

> [!Note]  
> Merge non ancora implementato. Pertanto, il valore di questo parametro viene ignorato.

 

</dd> <dt>

*LogString* \[ out\]
</dt> <dd>

Informazioni del log generate durante l'operazione di importazione.

</dd> </dl>

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

[**\_TSGatewayServer Win32**](win32-tsgatewayserver.md)
</dt> </dl>

 

