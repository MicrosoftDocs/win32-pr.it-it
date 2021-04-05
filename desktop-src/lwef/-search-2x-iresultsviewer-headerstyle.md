---
title: Proprietà HeaderStyle IResultsViewer (WdsView. h)
description: Stile dell'intestazione visualizzata nella visualizzazione.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà Header
- Proprietà Header, funzionalità dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà Header
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741594"
---
# <a name="iresultsviewerheaderstyle-property"></a>Proprietà IResultsViewer:: header

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Stile dell'intestazione visualizzata nella visualizzazione.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a>Valore proprietà

Imposta lo stile dell'intestazione visualizzata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





