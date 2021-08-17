---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b370c353cee43a001a35b8e5bd407547818d705e21334aff07d41e854f334cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066361"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Profilo di configurazione dm modem.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

**<ModemDMConfigProfile>**

## <a name="syntax"></a>Sintassi

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a>Chiave

`?`   facoltativo (zero o uno)

`*`   facoltativo (zero o più)

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

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
<td><a href="element-1-adminenable.md">AdminEnable</a></td>
<td><p>Specifica se il profilo è abilitato a livello amministrativo. Si tratta di un nuovo elemento per la versione 4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Specifica se il profilo è controllato dal roaming amministrativo. Questo elemento è nuovo per la versione 4. Il valore di questo elemento è un <a href="simpletype-roamcontroltype.md"><strong>valore roamControlType.</strong></a> Si tratta di un elemento facoltativo. se non viene specificato alcun valore, l'impostazione predefinita <strong>è AllRoamAllowed.</strong></p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">ApnID</a></td>
<td><p>ID APN associato a questo profilo. Questo elemento è nuovo nella versione 4 ed è facoltativo.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Contesto</a></td>
<td><p>Specifica i parametri necessari per stabilire una connessione dati.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Nome</a></td>
<td><p>Nome del profilo. Per altre informazioni, vedere la documentazione per l'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Nome</strong></a> v1.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">OemConnectionId</a></td>
<td><p>ID di connessione OEM per la configurazione dm del modem.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></td>
<td><p>Specifica la modalità di creazione del profilo dm del modem.</p>
<p>Questo valore viene usato per decidere se un utente può eliminare il profilo. Gli utenti possono eliminare <strong>solo i profili UserProvisioned.</strong></p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">RoamApplicability</a></td>
<td><p>Specifica che questo profilo è attivo solo quando la condizione di roaming corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">SimIccID</a></td>
<td><p>Numero di identificazione SIM per i dispositivi GSM. Per altre informazioni, vedere la documentazione per l'elemento <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

Questo elemento più esterno (documento) potrebbe non essere contenuto da altri elementi.

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

 

 



