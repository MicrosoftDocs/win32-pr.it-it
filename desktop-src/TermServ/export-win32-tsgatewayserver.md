---
title: Metodo Export della classe Win32_TSGatewayServer
description: Restituisce la configurazione del server Gateway Desktop remoto (Gateway Desktop remoto) come stringa XML.
ms.assetid: abf3a616-2b86-4cfe-934f-f1f17ce3ce31
ms.tgt_platform: multiple
keywords:
- Esporta il metodo Servizi Desktop remoto
- Metodo Export Servizi Desktop remoto, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Servizi Desktop remoto, metodo Export
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.Export
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429e27cb93c319e977d37926ac43488008d62714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964982"
---
# <a name="export-method-of-the-win32_tsgatewayserver-class"></a>Metodo Export della classe Win32 \_ TSGatewayServer

Restituisce la configurazione del server Gateway Desktop remoto (Gateway Desktop remoto) come stringa XML.

## <a name="syntax"></a>Sintassi


```mof
uint32 Export(
  [in]  uint32 ExportType,
  [out] string XmlString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ExportType* \[ in\]
</dt> <dd>

Contenuto da esportare. Impostare il tipo di esportazione impostando i bit corrispondenti nel parametro *ExportType* . È possibile impostare più tipi di esportazione. Se, ad esempio, è impostato il bit 0, verranno esportati Servizi Desktop remoto i criteri di autorizzazione della connessione. Se è impostato sia il bit 0 che il secondo bit, verranno esportati sia i criteri di autorizzazione connessioni Desktop remoto che i criteri di autorizzazione risorse Servizi Desktop remoto.

<dt>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>

<span id="Export_all_CAPs"></span><span id="export_all_caps"></span><span id="EXPORT_ALL_CAPS"></span>**Esporta tutti i limiti** (1)


</dt> <dd>

Esporta tutti i tappi desktop remoto.

</dd> <dt>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>

<span id="Export_all_Radius_Servers"></span><span id="export_all_radius_servers"></span><span id="EXPORT_ALL_RADIUS_SERVERS"></span>**Esporta tutti i server RADIUS** (2)


</dt> <dd>

Esportare un elenco di tutti i server dei criteri di rete (NPS).

</dd> <dt>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>

<span id="Export_all_RAPs"></span><span id="export_all_raps"></span><span id="EXPORT_ALL_RAPS"></span>**Esporta tutti i rap** (4)


</dt> <dd>

Esporta tutti i rap RD.

</dd> <dt>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>

<span id="Export_all_RGs"></span><span id="export_all_rgs"></span><span id="EXPORT_ALL_RGS"></span>**Esporta tutti i RGS** (8)


</dt> <dd>

Esportare tutti i gruppi di risorse.

</dd> <dt>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>

<span id="Export_all_LoadBalancing_Servers"></span><span id="export_all_loadbalancing_servers"></span><span id="EXPORT_ALL_LOADBALANCING_SERVERS"></span>**Esporta tutti i Server Loadbalancing** (16)


</dt> <dd>

Esportare un elenco di tutti i server di bilanciamento del carico.

</dd> <dt>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>

<span id="Export_all_Server_Settings"></span><span id="export_all_server_settings"></span><span id="EXPORT_ALL_SERVER_SETTINGS"></span>**Esporta tutte le impostazioni del server** (32)


</dt> <dd>

Esportare tutte le impostazioni del server correlate a Gateway Desktop remoto.

</dd> <dt>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>

<span id="Export_all_Health_Policies"></span><span id="export_all_health_policies"></span><span id="EXPORT_ALL_HEALTH_POLICIES"></span>**Esporta tutti i criteri di integrità** (64)


</dt> <dd>

Esportare tutti i criteri di integrità.

* * Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 e Windows Server 2008: * *

Questo valore non è supportato prima di Windows Server 2016.

</dd> </dl> </dd> <dt>

*XmlString* \[ out\]
</dt> <dd>

Stringa dell'XML.

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

 

