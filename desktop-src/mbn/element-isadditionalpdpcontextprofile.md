---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a075916144971196433d1a490a9076c4d40ddb86b363d2904d1affce63a5995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745123"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

**L'elemento IsAdditionalPdpContextProfile** contiene un valore booleano **che** è true se si tratta di un profilo "contesto PDP (Packet Data Protocol) aggiuntivo" e **false**, in caso contrario.  Il valore predefinito **è false.**

Un profilo "contesto PDP aggiuntivo" è un profilo che non viene attivato sulla porta predefinita della scheda fisica e l'impostazione di questo elemento su true garantisce che questo profilo non sia visualizzato in modo non appropriato nell'interfaccia utente.

Si noti che se questo elemento è impostato su true, deve essere true anche quanto segue.

-   [**L'elemento IsDefault**](./schema-isdefault-mbnprofile-element.md) deve essere non specificato o impostato su **false** perché il profilo sia valido.
-   [**L'elemento ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) deve essere non specificato o impostato su **manual** perché il profilo sia valido.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a>Sintassi

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

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
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
