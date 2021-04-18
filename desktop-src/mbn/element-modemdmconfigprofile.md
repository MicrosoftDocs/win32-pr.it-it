---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306790"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Profilo di configurazione modem DM.

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
<td><a href="element-1-adminenable.md">AdminEnable</a></td>
<td><p>Specifica se il profilo è abilitato in amministrazione. Si tratta di un nuovo elemento per V4.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></td>
<td><p>Specifica se il profilo è gestito dal roaming amministrativo. Questo elemento è nuovo per V4. Il valore di questo elemento è un valore <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> . Si tratta di un elemento facoltativo. Se non viene specificato alcun valore, <strong>AllRoamAllowed</strong> è il valore predefinito.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-apnid.md">ApnID</a></td>
<td><p>ID APN associato a questo profilo. Questo elemento è una novità di V4 ed è facoltativo.</p></td>
</tr>
<tr class="even">
<td><a href="element-1-context.md">Contesto</a></td>
<td><p>Specifica i parametri necessari per stabilire una connessione dati.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-name.md">Nome</a></td>
<td><p>Nome del profilo. Per ulteriori informazioni, vedere la documentazione relativa all'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>nome</strong></a> V1.</p></td>
</tr>
<tr class="even">
<td><a href="element-oemconnectionid.md">OemConnectionId</a></td>
<td><p>ID di connessione OEM per la configurazione del modem DM.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></td>
<td><p>Specifica il modo in cui è stato creato il profilo DM del modem.</p>
<p>Questo valore viene usato per decidere se un utente può eliminare il profilo. Gli utenti possono eliminare solo i profili <strong>UserProvisioned</strong> .</p></td>
</tr>
<tr class="even">
<td><a href="element-1-roamapplicability.md">RoamApplicability</a></td>
<td><p>Specifica che il profilo è attivo solo quando la condizione di roaming corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere utilizzato per attivare un contesto del protocollo PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</p></td>
</tr>
<tr class="odd">
<td><a href="element-1-simiccid.md">SimIccID</a></td>
<td><p>Numero di identifcation SIM per i dispositivi GSM. Per altri dettagli, vedere la documentazione per l'elemento V1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> .</p></td>
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

 

 



