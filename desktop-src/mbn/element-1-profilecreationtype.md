---
description: ProfileCreationType (in ModemDMConfigProfile)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (in ModemDMConfigProfile)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b755840d0308ec2d7a7bba5896b0cf67b7b61198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879158"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)

Specifica il modo in cui è stato creato il profilo DM del modem.

Questo valore viene usato per decidere se un utente può eliminare il profilo. Gli utenti possono eliminare solo i profili **UserProvisioned** .

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a>Sintassi

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuna.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuna.

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
<td><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></td>
<td><p>Profilo di configurazione modem DM.</p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a>Elementi correlati

Gli elementi seguenti hanno lo stesso nome di questo elemento, ma il contenuto o gli attributi sono diversi:

-   **[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**

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

 

 



