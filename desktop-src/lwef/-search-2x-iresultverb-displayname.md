---
title: Proprietà DisplayName IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048217"
---
# <a name="iresultverbdisplayname-property"></a>IResultVerb::D proprietà di riproduzione

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





