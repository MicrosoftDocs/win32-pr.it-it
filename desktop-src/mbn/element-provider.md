---
description: Provider
MS-HAID: WWAN\_profile\_v4.element\_Provider
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Provider
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a701c4dd-967f-4f03-ada4-d34059f5a1e4
api_name:
- Provider
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2d9208e3c0aad7ab05348056eaf70747aa23433e0ab5badec5da1f2baf063b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066307"
---
# <a name="span-idwwan_profile_v4element_providerspanprovider"></a><span id="WWAN_profile_v4.element_Provider"></span>Provider

Specifica un provider di rete preferito in un elenco di provider da usare durante il roaming.

Il valore di questo elemento è un'istanza del tipo complesso [**providerType**](./schema-providertype-complextype.md) v1.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[<MBNProfileExt>](element-mbnprofileext.md)  
[<DataRoamingPartners>](element-dataroamingpartners.md)  
**<Provider>**

## <a name="syntax"></a>Sintassi

``` syntax
<Provider>

  providerType

</Provider>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

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
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>Specifica un elenco di provider di rete preferiti durante il roaming.</p>
<p>Per informazioni dettagliate, vedere la documentazione per <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>l'elemento DataRoamingPartners v1.</strong></a></p></td>
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

 

 
