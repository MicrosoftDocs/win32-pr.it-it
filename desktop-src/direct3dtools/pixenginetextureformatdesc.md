---
description: Rappresenta una descrizione di un formato di trama.
MS-HAID: vspixengine.PixEngineTextureFormatDesc
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixEngineTextureFormatDesc
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 685DC746-544D-4ACB-AB1F-9FA62C5CF416
api_name:
- PixEngineTextureFormatDesc
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 960186f0c28be88805c1df65f1a517c4ce4a4c64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965717"
---
# <a name="span-idvspixenginepixenginetextureformatdescspanpixenginetextureformatdesc-structure"></a><span id="vspixengine.pixenginetextureformatdesc"></span>Struttura PixEngineTextureFormatDesc

Rappresenta una descrizione di un formato di trama.

## <a name="syntax"></a>Sintassi


```C++
} PixEngineTextureFormatDesc;
```

## <a name="members"></a>Members

**dxgiFormat**  
Formato DXGI della trama.

**dataFormat**  
Formato dati della trama.

**blockBytes**  
Numero di byte in un blocco di dati.

**blockHeight**  
Altezza (esempi di numero nell'asse Y) del blocco.

**blockWidth**  
Larghezza (numero di campioni nell'asse X) del blocco.

**channelX**  
Descrive le proprietà del canale X. Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.

**canale**  
Descrive le proprietà del canale Y. Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.

**channelZ**  
Descrive le proprietà del canale Z. Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.

**channelW**  
Descrive le proprietà del canale W. Per ulteriori informazioni, vedere la struttura PixEngineChannelDescription.

**swizzle**  
Viene descritto il swizzle (swapping del canale) applicato all'esempio.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



