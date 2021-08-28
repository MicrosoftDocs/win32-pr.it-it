---
description: MBNProfileExt \/ ... \/ AuthProtocol (v4)
MS-HAID: WWAN\_profile\_v4.element\_AuthProtocol
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: AuthProtocol
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8274effe-1fcc-43f8-a609-795fe19a1c4f
api_name:
- AuthProtocol
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 487c58bda5e3b891b0e14614fa6c91830bc7512e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482737"
---
# <a name="span-idwwan_profile_v4element_authprotocolspanmbnprofileextauthprotocol-v4"></a><span id="WWAN_profile_v4.element_AuthProtocol"></span>MBNProfileExt \/ ... \/ AuthProtocol (v4)

>Specifica il protocollo di autenticazione da usare per attivare un contesto PDP (Packet Data Protocol).

Si noti che nella versione 4 è disponibile un nuovo valore di enumerazione per questo elemento. **AutoSelection** significa che un protocollo di autenticazione deve essere selezionato dai livelli inferiori.

Per altre informazioni, vedere la documentazione per l'elemento [**AuthProtocol**](./schema-authprotocol-contexttype-element.md) v1.

## <a name="element-hierarchy"></a>Gerarchia degli elementi

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<AuthProtocol\>**

## <a name="syntax"></a>Sintassi

``` syntax
<AuthProtocol>

  "NONE" | "PAP" | "CHAP" | "MsCHAPv2" | "AutoSelection"

</AuthProtocol>
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


 

 
