---
title: Proprietà HelpText IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce un puntatore alla stringa della Guida localizzata per il verbo.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- Funzionalità della proprietà HelpText ambiente Windows legacy
- Proprietà HelpText caratteristiche dell'ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà HelpText
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741034"
---
# <a name="iresultverbhelptext-property"></a>Proprietà IResultVerb:: HelpText

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà restituisce un puntatore alla stringa della Guida localizzata per il verbo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un puntatore alla stringa della Guida localizzata per questo verbo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





