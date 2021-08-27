---
description: MBNProfileExt \/ ... \/ IPType (v4)
MS-HAID: WWAN\_profile\_v4.element\_IPType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7823fc62bea228ec2a1f7e50629d74ce29dde3
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988754"
---
# <a name="span-idwwan_profile_v4element_iptypespanmbnprofileextiptype-v4"></a><span id="WWAN_profile_v4.element_IPType"></span>MBNProfileExt \/ ... \/ IPType (v4)

Specifica il tipo di IP da utilizzare in questa connessione dati.

Questo elemento è una novità nella versione 4 dello schema. L'elemento può avere uno dei valori seguenti.

| Valore   | Significato                                       |
|---------|-----------------------------------------------|
| Predefinito | Il tipo di IP deve essere selezionato dai livelli inferiori     |
| IPv4    | Usare IPv4                                      |
| IPv6    | Utilizza IPv6                                      |
| IPv4v6  | Usare IPv4 e/o IPv6, come disponibile.           |
| A QUESTOREA    | Usare 464XLAT per eseguire il tunneling di IPv4 su reti IPv6 |

 

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<IPType\>**

## <a name="syntax"></a>Sintassi

``` syntax
<IPType>

  "Default" | "IPv4" | "IPv6" | "IPv4v6" | "XLAT"

</IPType>
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


| Requisito | Valore |
|------------|----------|
| <p>Spazio dei nomi</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 



