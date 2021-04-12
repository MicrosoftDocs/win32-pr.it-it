---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343356"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

L'elemento **IsAdditionalPdpContextProfile** contiene un **valore booleano** che è **true** se si tratta di un profilo "contesto aggiuntivo PDP (Packet Data Protocol)" e **false**, in caso contrario. Il valore predefinito è **false**.

Un profilo "contesto PDP aggiuntivo" è un profilo che non viene attivato sulla porta predefinita della scheda fisica e l'impostazione di questo elemento su true garantisce che il profilo non venga visualizzato in modo non appropriato nell'interfaccia utente.

Si noti che se questo elemento è impostato su true, deve essere true anche quanto segue.

-   L'elemento [**IsDefault**](./schema-isdefault-mbnprofile-element.md) deve essere non specificato o impostato su **false** affinché il profilo sia valido.
-   L'elemento [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) non deve essere specificato o impostato su **Manual** affinché il profilo sia valido.

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

Nessuna.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuna.

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
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
