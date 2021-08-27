---
description: ProfileCreationType (in MBNProfileExt)
MS-HAID: WWAN\_profile\_v4.element\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (in MBNProfileExt)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652d406689219c8a535e0a75ae7123180c7530a6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885410"
---
# <a name="span-idwwan_profile_v4element_profilecreationtypespanprofilecreationtype-in-mbnprofileext"></a><span id="WWAN_profile_v4.element_ProfileCreationType"></span>ProfileCreationType (in MBNProfileExt)

Specifica l'autore del profilo.

Per altre informazioni su questo elemento, vedere la documentazione per l'elemento [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) v1.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;ProfileCreationType&gt;**

## <a name="syntax"></a>Sintassi

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p><strong>L'elemento MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo Mobile Broadband con un set più ricco di opzioni rispetto all'elemento MBNProfile.</p><p>In un profilo possono essere presenti più elementi MbnProfileExt che descrivono le impostazioni del profilo per un determinato set di condizioni operative. Usare <a href="element-profileconditionedon.md"><strong>l'elemento figlio ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.</p> | 


 

## <a name="related-elements"></a>Elementi correlati

Gli elementi seguenti hanno lo stesso nome di questo elemento, ma il contenuto o gli attributi sono diversi:

-   **[ProfileCreationType (in ModemDMConfigProfile)](element-1-profilecreationtype.md)**

## <a name="requirements"></a>Requisiti


| | | <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
