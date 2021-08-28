---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80684cdf2d47d203318afbfd7b5e6bc02de1d3dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982744"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile

Profilo di configurazione dm modem.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

**&lt;ModemDMConfigProfile&gt;**

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


| Elemento figlio | Descrizione | 
|---------------|-------------|
| <a href="element-1-adminenable.md">AdminEnable</a> | <p>Specifica se il profilo è abilitato a livello amministrativo. Si tratta di un nuovo elemento per la versione 4.</p> | 
| <a href="element-1-adminroamcontrol.md">AdminRoamControl</a> | <p>Specifica se il profilo è controllato dal roaming amministrativo. Questo elemento è nuovo per la versione 4. Il valore di questo elemento è un <a href="simpletype-roamcontroltype.md"><strong>valore roamControlType.</strong></a> Si tratta di un elemento facoltativo. se non viene specificato alcun valore, l'impostazione predefinita è <strong>AllRoamAllowed.</strong></p> | 
| <a href="element-1-apnid.md">ApnID</a> | <p>ID APN associato a questo profilo. Questo elemento è nuovo nella versione 4 ed è facoltativo.</p> | 
| <a href="element-1-context.md">Contesto</a> | <p>Specifica i parametri necessari per stabilire una connessione dati.</p> | 
| <a href="element-1-name.md">Nome</a> | <p>Nome del profilo. Per altre informazioni, vedere la documentazione per l'elemento <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Nome</strong></a> v1.</p> | 
| <a href="element-oemconnectionid.md">OemConnectionId</a> | <p>ID di connessione OEM per la configurazione dm del modem.</p> | 
| <a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a> | <p>Specifica la modalità di creazione del profilo dm del modem.</p><p>Questo valore viene usato per decidere se un utente può eliminare il profilo. Gli utenti possono eliminare <strong>solo i profili UserProvisioned.</strong></p> | 
| <a href="element-1-roamapplicability.md">RoamApplicability</a> | <p>Specifica che questo profilo è attivo solo quando la condizione di roaming corrente è quella specificata. In caso contrario, il profilo non è applicabile e non può essere usato per attivare un contesto PDP (Packet Data Protocol). Il valore di questo elemento deve essere un valore <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> valido.</p> | 
| <a href="element-1-simiccid.md">SimIccID</a> | <p>Numero di identificazione SIM per i dispositivi GSM. Per altre informazioni, vedere la documentazione per l'elemento <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> v1.</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre

Questo elemento più esterno (documento) potrebbe non essere contenuto da altri elementi.

## <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



