---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343781"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

L'elemento **MBNProfileExt** è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo a banda larga mobile con un set di opzioni più completo rispetto all'elemento MBNProfile.

In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare l'elemento figlio [**ProfileConditionedOn**](element-profileconditionedon.md) di **MBNProfileExt** per specificare le condizioni operative che rendono il profilo attivo un profilo specifico.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

**<MBNProfileExt>**

## <a name="syntax"></a>Sintassi

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a>Chiave

`?`   facoltativo (zero o uno)

`*`   facoltativo (zero o più)

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
<td><a href="element-adminenable.md">AdminEnable</a></td>
<td><p>Specifica se il profilo è abilitato in amministrazione. Si tratta di un nuovo elemento per V4.</p></td>
</tr>
<tr class="even">
<td><a href="element-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Specifica se il profilo è gestito dal roaming amministrativo. Questo elemento è nuovo per V4. Il valore di questo elemento è un valore <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Si tratta di un elemento facoltativo. Se non viene specificato alcun valore, <strong>AllRoamAllowed</strong> è il valore predefinito.</p></td>
</tr>
<tr class="odd">
<td><a href="element-apnid.md">ApnID</a></td>
<td><p>ID APN associato a questo profilo. Questo elemento è una novità di V4 ed è facoltativo.</p></td>
</tr>
<tr class="even">
<td><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></td>
<td><p>Specifica se il dispositivo mobile broadband si connetterà automaticamente a una rete.</p>
<p>Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-connectionmode.md">ConnectionMode</a></td>
<td><p>Specifica l'impostazione di connessione automatica da usare per un dispositivo mobile broadband.</p>
<p>Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-context.md">Contesto</a></td>
<td><p>Specifica i parametri necessari per stabilire una connessione dati.</p></td>
</tr>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Specifica un elenco di provider di rete preferiti durante il roaming.</p>
<p>Per informazioni dettagliate, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-description.md">Descrizione</a></td>
<td><p>Descrizione del profilo.</p></td>
</tr>
<tr class="odd">
<td><a href="element-homeprovidername.md">HomeProviderName</a></td>
<td><p>Nome del provider Home per la SIM/dispositivo specificato. Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> .</p></td>
</tr>
<tr class="even">
<td><a href="element-iconfilepath.md">ICONFilePath</a></td>
<td><p>Percorso del file di icona per la connessione. L'interfaccia utente di connessione al sistema operativo Visualizza l'icona quando viene eseguita una connessione utilizzando questo profilo.</p>
<p>Per ulteriori informazioni sull'utilizzo di questo elemento, vedere la documentazione V1 relativa a <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</p></td>
</tr>
<tr class="odd">
<td><a href="element-isdefault.md">IsDefault</a></td>
<td><p>Specifica se il profilo è il profilo predefinito.</p>
<p>Per informazioni più dettagliate su questo elemento, vedere la documentazione V1 per <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</p></td>
</tr>
<tr class="even">
<td><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></td>
<td><p>Specifica che il profilo è esclusivo per gli altri profili degli stessi set di profili. Questo elemento è nuovo per V4.</p></td>
</tr>
<tr class="odd">
<td><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></td>
<td><p>Specifica che questo profilo è un profilo di contesto PDP aggiuntivo di lunga durata. Se il valore di questo elemento è <strong>true</strong>, anche <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true</strong>. Si tratta di un nuovo elemento per V4.</p></td>
</tr>
<tr class="even">
<td><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></td>
<td><p>Specifica che il profilo deve essere usato solo per il provisioning. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol). Questo elemento è nuovo per V4.</p>
<p>Se <strong>IsProvisioningProfile</strong> è true, l' <a href="element-isdefault.md"><strong>impostazione predefinita</strong></a> deve essere false e <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> deve essere manuale.</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmsconfiguration.md">MmsConfiguration</a></td>
<td><p>Informazioni di configurazione per il servizio messaggistica multimediale (MMS).</p>
<p>Oltre a impostare gli elementi di configurazione all'interno di questo elemento, un profilo MMS deve avere le impostazioni seguenti.</p>
<ul>
<li>L'elemento <a href="element-name.md"><strong>Name</strong></a> deve contenere un nome univoco a livello di sistema.</li>
<li>Il relativo <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve essere impostato su <strong>UserProvisioned</strong>.</li>
<li>Il <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve contenere il ICCID della SIM a cui è destinato questo profilo.</li>
<li>Il relativo <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> deve essere impostato su <strong>Manual</strong>.</li>
<li>Il <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve contenere il GUID per il gruppo di scopi di MMS.</li>
<li>Il valore di <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="element-name.md">Nome</a></td>
<td><p>Nome del profilo. Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nome</strong></a> V1.</p></td>
</tr>
<tr class="odd">
<td><a href="element-profileconditionedon.md">ProfileConditionedOn</a></td>
<td><p>Specifica le condizioni che devono essere soddisfatte per l'applicazione di un profilo.</p>
<p>Questo elemento è nuovo per V4. Consente di specificare più profili che si applicano a condizioni diverse e che il profilo appropriato venga utilizzato automaticamente quando è applicabile. Questo elemento è facoltativo. Se non viene specificato, il profilo è sempre applicabile rispetto alle condizioni elencate.</p></td>
</tr>
<tr class="even">
<td><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></td>
<td><p>Specifica l'autore del profilo.</p>
<p>Per ulteriori informazioni su questo elemento, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-purposegroups.md">PurposeGroups</a></td>
<td><p>Elenco facoltativo di gruppi di profili, in cui ogni gruppo include i profili utilizzati per uno scopo comune.</p>
<p>Questo elemento è nuovo per la V4 dello schema.</p>
<p>Un profilo può essere elencato in più gruppi.</p></td>
</tr>
<tr class="even">
<td><a href="element-simiccid.md">SimIccID</a></td>
<td><p>Numero di identifcation SIM per i dispositivi GSM. Per altri dettagli, vedere la documentazione per l'elemento V1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> .</p></td>
</tr>
<tr class="odd">
<td><a href="element-subscriberid.md">SubscriberID</a></td>
<td><p>Identifica l'identificatore univoco del profilo.</p>
<p>Per una rete GSM questo deve contenere IMSI (International Mobile Subscriber Identity) della SIM e per i dispositivi CDMA deve contenere il numero minimo di identificazione mobile del dispositivo.</p>
<p>Per ulteriori informazioni, vedere la documentazione relativa all'elemento V1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> .</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

Questo elemento (documento) più esterno potrebbe non essere contenuto da altri elementi.

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

 

 
