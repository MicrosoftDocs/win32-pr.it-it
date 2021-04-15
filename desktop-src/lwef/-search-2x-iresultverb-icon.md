---
title: Proprietà Icon IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce un puntatore per gestire l'icona facoltativa associata al verbo.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Proprietà icona caratteristiche ambiente Windows legacy
- Proprietà icona caratteristiche ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà Icon
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477668"
---
# <a name="iresultverbicon-property"></a>Proprietà IResultVerb:: icon

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà restituisce un puntatore per gestire l'icona facoltativa associata al verbo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a>Valore proprietà

Hicon è un puntatore all'handle dell'icona facoltativa assocuated con il verbo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





