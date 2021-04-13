---
description: '\/Contesto ModemDMConfigProfile (v4)'
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Context
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d89bee5847885068a3a7d072f820c6794a3dbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484860"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span id="WWAN_profile_v4.element_1_Context"></span>\/Contesto ModemDMConfigProfile (v4)

Specifica i parametri necessari per stabilire una connessione dati.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a>Sintassi

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a>Chiave

`?`   facoltativo (zero o uno)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuna.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento figlio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-1-accessstring.md">AccessString</a></td>
<td><p>Identifica l'APN o la stringa di connessione da utilizzare per stabilire una connessione dati.</p>
<p>Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-1-authprotocol.md">AuthProtocol</a></td>
<td><p>>Specifica il protocollo di autenticazione da utilizzare per l'attivazione di un contesto del protocollo PDP (Packet Data Protocol).</p>
<p>Si noti che in V4 è disponibile un nuovo valore di enumerazione per questo elemento. La <strong>selezione di autoselezione</strong> indica che un protocollo di autenticazione deve essere prelevato da uno o più livelli inferiori.</p>
<p>Per ulteriori informazioni, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-compression.md">Compressione</a></td>
<td><p>Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.</p>
<p>Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> V1.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-iptype.md">IPType</a></td>
<td><p>Specifica il tipo di IP da utilizzare per la connessione dati.</p>
<p>Questo elemento è nuovo in V4 dello schema. L'elemento può avere uno dei valori seguenti.</p>
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Predefinito</td>
<td>Il tipo di IP deve essere prelevato da uno o più livelli inferiori</td>
</tr>
<tr class="even">
<td>IPv4</td>
<td>USA IPv4</td>
</tr>
<tr class="odd">
<td>IPv6</td>
<td>Utilizza IPv6</td>
</tr>
<tr class="even">
<td>IPv4v6</td>
<td>Utilizzare IPv4 e/o IPv6 come disponibile.</td>
</tr>
<tr class="odd">
<td>XLAT</td>
<td>Usare 464XLAT per eseguire il tunneling IPv4 su reti IPv6</td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><a href="element-1-userlogoncred.md">UserLogonCred</a></td>
<td><p>Credenziali di accesso per una connessione.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento padre</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p>L'elemento <strong>MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.</p>
<p>In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare l'elemento figlio <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.</p></td>
</tr>
<tr class="even">
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Profilo di configurazione modem DM.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisiti

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Spazio dei nomi</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



