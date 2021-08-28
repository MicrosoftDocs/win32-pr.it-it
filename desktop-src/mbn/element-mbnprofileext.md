---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac9167561aabe151b75a4aa295a1c8aacec974df
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884074"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt

**L'elemento MBNProfileExt** è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo Mobile Broadband con un set di opzioni più ricco rispetto all'elemento MBNProfile.

In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un particolare set di condizioni operative. Usare [**l'elemento figlio ProfileConditionedOn**](element-profileconditionedon.md) di **MBNProfileExt** per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

**&lt;MBNProfileExt&gt;**

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

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio


| Elemento figlio | Descrizione | 
|---------------|-------------|
| <a href="element-adminenable.md">AdminEnable</a> | <p>Specifica se il profilo è abilitato a livello amministrativo. Si tratta di un nuovo elemento per v4.</p> | 
| <a href="element-adminroamcontrol.md">AdminRoamControl</a> | <p>Specifica se il profilo è controllato dal roaming amministrativo. Questo elemento è una novità per v4. Il valore di questo elemento è un <a href="simpletype-roamcontroltype.md"><strong>valore roamControlType.</strong></a> Si tratta di un elemento facoltativo. Se non viene specificato alcun valore, <strong>AllRoamAllowed è</strong> l'impostazione predefinita.</p> | 
| <a href="element-apnid.md">APNID</a> | <p>ID APN associato a questo profilo. Questo elemento è una novità della versione 4 ed è facoltativo.</p> | 
| <a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a> | <p>Specifica se il dispositivo Mobile Broadband si connetterà automaticamente a una rete.</p><p>Per altre informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> v1.</p> | 
| <a href="element-connectionmode.md">ConnectionMode</a> | <p>Specifica l'impostazione di connessione automatica da usare per un dispositivo Mobile Broadband.</p><p>Per altre informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> v1.</p> | 
| <a href="element-context.md">Contesto</a> | <p>Specifica i parametri necessari per stabilire una connessione dati.</p> | 
| <a href="element-dataroamingpartners.md">DataRoamingPartners</a> | <p>Specifica un elenco di provider di rete preferiti durante il roaming.</p><p>Per informazioni dettagliate, vedere la documentazione per <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>l'elemento DataRoamingPartners</strong></a> v1.</p> | 
| <a href="element-description.md">Descrizione</a> | <p>Descrizione del profilo.</p> | 
| <a href="element-homeprovidername.md">HomeProviderName</a> | <p>Nome del provider principale per la SIM/dispositivo specificata. Per altre informazioni, vedere la documentazione per l'elemento <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> v1.</p> | 
| <a href="element-iconfilepath.md">ICONFilePath</a> | <p>Percorso del file dell'icona per la connessione. L'interfaccia utente di connessione del sistema operativo visualizza l'icona quando viene stabilita una connessione tramite questo profilo.</p><p>Per altri dettagli sull'uso di questo elemento, vedere la documentazione v1 per <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath.</strong></a></p> | 
| <a href="element-isdefault.md">IsDefault</a> | <p>Specifica se questo profilo è il profilo predefinito.</p><p>Per altri dettagli su questo elemento, vedere la documentazione v1 per <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault.</strong></a></p> | 
| <a href="element-isexclusivetoother.md">IsExclusiveToOther</a> | <p>Specifica che questo profilo è esclusivo per altri profili degli stessi set di profili. Questo elemento è una novità per v4.</p> | 
| <a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a> | <p>Specifica che questo profilo è un profilo di contesto PDP aggiuntivo di lunga data. Se il valore di questo elemento è <strong>true,</strong> <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>anche IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true.</strong> Si tratta di un nuovo elemento per v4.</p> | 
| <a href="element-isprovisioningprofile.md">IsProvisioningProfile</a> | <p>Specifica che questo profilo deve essere usato solo per il provisioning. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol). Questo elemento è una novità per v4.</p><p>Se <strong>IsProvisioningProfile</strong> è true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> deve essere false e <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> deve essere manuale.</p> | 
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Informazioni di configurazione per MmS (Multimedia Messaging Service).</p><p>Oltre a impostare gli elementi di configurazione all'interno di questo elemento, un profilo MMS deve avere le impostazioni seguenti.</p><ul><li><a href="element-name.md"><strong>L'elemento Name</strong></a> deve contenere un nome univoco a livello di sistema.</li><li><a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType deve</strong></a> essere impostato su <strong>UserProvisioned.</strong></li><li><a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID deve</strong></a> contenere l'ICCID della SIM a cui è destinato questo profilo.</li><li>ConnectionMode <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>deve</strong></a> essere impostato su <strong>Manual.</strong></li><li><a href="element-purposegroupguid.md"><strong>PurposeGroupGuid deve</strong></a> contenere il GUID per il gruppo di scopi MMS.</li><li><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true.</strong></li></ul> | 
| <a href="element-name.md">Nome</a> | <p>Nome del profilo. Per altre informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name v1.</strong></a></p> | 
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>Specifica le condizioni che devono essere soddisfatte perché un profilo sia applicabile.</p><p>Questo elemento è una novità per v4. Consente di specificare più profili che si applicano in condizioni diverse e di usare automaticamente il profilo appropriato quando è applicabile. Questo elemento è facoltativo. Se non viene specificato, il profilo è sempre applicabile in relazione alle condizioni elencate.</p> | 
| <a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a> | <p>Specifica l'autore del profilo.</p><p>Per altre informazioni su questo elemento, vedere la documentazione relativa all'elemento <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> v1.</p> | 
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>Elenco facoltativo di gruppi di profili, in cui ogni gruppo include i profili usati per uno scopo comune.</p><p>Questo elemento è una novità per la versione 4 dello schema.</p><p>Un profilo può essere elencato in più gruppi.</p> | 
| <a href="element-simiccid.md">SimIccID</a> | <p>Numero di identificazione SIM per i dispositivi GSM. Per altri dettagli, vedere la documentazione per <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>l'elemento SimIccID</strong></a> v1.</p> | 
| <a href="element-subscriberid.md">SubscriberID</a> | <p>Identifica l'identificatore univoco del profilo.</p><p>Per una rete GSM deve contenere l'IMSI (International Mobile Subscriber Identity) della SIM e per i dispositivi CDMA deve contenere il valore MIN (Mobile Identification Number) del dispositivo.</p><p>Per altre informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

Questo elemento più esterno (documento) potrebbe non essere contenuto da altri elementi.

## <a name="requirements"></a>Requisiti


| | | <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
