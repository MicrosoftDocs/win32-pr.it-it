---
description: MmscPort
MS-HAID: WWAN\_profile\_v4.element\_MmscPort
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscPort
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56077222bbc738e9f735a9068cc81f0bfebc8463
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885430"
---
# <a name="span-idwwan_profile_v4element_mmscportspanmmscport"></a><span id="WWAN_profile_v4.element_MmscPort"></span>MmscPort

Specifica il numero di porta del server MMSC per il dispositivo. Specificare 0 per indicare che non è specificata alcuna porta specifica. facoltativo.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;MmsConfiguration&gt;](element-mmsconfiguration.md)  
**&lt;MmscPort&gt;**

## <a name="syntax"></a>Sintassi

``` syntax
<MmscPort>

  [TBD (missing description)]

</MmscPort>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>Informazioni di configurazione per MmS (Multimedia Messaging Service).</p><p>Oltre a impostare gli elementi di configurazione all'interno di questo elemento, un profilo MMS deve avere le impostazioni seguenti.</p><ul><li><a href="element-name.md"><strong>L'elemento Name</strong></a> deve contenere un nome univoco a livello di sistema.</li><li><a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> deve essere impostato su <strong>UserProvisioned.</strong></li><li><a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> deve contenere l'ICCID della SIM a cui è destinato questo profilo.</li><li>ConnectionMode <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>deve</strong></a> essere impostato su <strong>Manual.</strong></li><li><a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> deve contenere il GUID per il gruppo di scopi MMS.</li><li><a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> deve essere impostato su <strong>true.</strong></li></ul> | 


 

## <a name="requirements"></a>Requisiti


| | | <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
