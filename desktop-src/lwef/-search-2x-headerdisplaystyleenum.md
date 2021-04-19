---
title: Enumerazione HeaderDisplayStyle
description: Usato da IResultsViewer HeaderStyle per impostare o restituire lo stile dell'intestazione corrente.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione HeaderDisplayStyle
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327864"
---
# <a name="headerdisplaystyle-enumeration"></a>Enumerazione HeaderDisplayStyle

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Usato da [**IResultsViewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) per impostare o restituire lo stile dell'intestazione corrente.

## <a name="syntax"></a>Sintassi


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**
</dt> <dd>

Indica o imposta l'utilizzo di intestazioni complete.

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**
</dt> <dd>

Indica o imposta l'utilizzo di intestazioni Compact.

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**
</dt> <dd>

Indica o imposta l'utilizzo di nessuna intestazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|----------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





