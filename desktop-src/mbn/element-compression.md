---
description: MBNProfileExt \/ ... \/ Compressione (v4)
MS-HAID: WWAN\_profile\_v4.element\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Compressione
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4b2ad853-ecb3-46ef-8ce2-aa001bb070e6
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc034b12a6a3375c9881a1fd3709d78be2e79a15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478237"
---
# <a name="span-idwwan_profile_v4element_compressionspanmbnprofileextcompression-v4"></a><span id="WWAN_profile_v4.element_Compression"></span>MBNProfileExt \/ ... \/ Compressione (v4)

Specifica se la compressione verrà utilizzata nel collegamento dati per l'intestazione e il trasferimento dei dati.

Per altre informazioni, vedere la documentazione relativa all'elemento [**Compression**](./schema-compression-contexttype-element.md) v1.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a>Sintassi

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributi ed elementi

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi

Nessuno.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementi figlio

Nessuno.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementi padre


| Elemento padre | Descrizione | 
|----------------|-------------|
| <a href="element-context.md">Contesto</a> | <p>Specifica i parametri necessari per stabilire una connessione dati.</p> | 


 

## <a name="requirements"></a>Requisiti


| | | <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
