---
description: Descrizione (Mobile Broadband) - Descrizione
MS-HAID: WWAN\_profile\_v4.element\_Description
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Descrizione (Mobile Broadband)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7adc4b26-1202-4f80-8b26-7879df687bb0
api_name:
- Description
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e57e8127a4de492ba4644505237cf6d8975b89db
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986294"
---
# <a name="description-mobile-broadband"></a>Descrizione (Mobile Broadband)

Descrizione del profilo.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
**&lt;Descrizione&gt;**

## <a name="syntax"></a>Sintassi

``` syntax
<Description>

  nameType

</Description>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p><strong>L'elemento MBNProfileExt</strong> è un'estensione dell'elemento MBNProfile precedente. Identifica un profilo Mobile Broadband con un set di opzioni più ricco rispetto all'elemento MBNProfile.</p><p>In un profilo possono essere presenti più elementi MbnProfileExt, che descrivono le impostazioni del profilo per un particolare set di condizioni operative. Usare <a href="element-profileconditionedon.md"><strong>l'elemento figlio ProfileConditionedOn</strong></a> di <strong>MBNProfileExt</strong> per specificare le condizioni operative che rendono un profilo specifico il profilo attivo.</p> | 


 

## <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



