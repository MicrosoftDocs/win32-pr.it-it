---
title: Proprietà IResultsViewer PreviewStyle (WdsView. h)
description: Controlla la modalità di visualizzazione del riquadro di anteprima.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà PreviewStyle
- Proprietà PreviewStyle caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, Proprietà PreviewStyle
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301037"
---
# <a name="iresultsviewerpreviewstyle-property"></a>IResultsViewer::P proprietà reviewStyle

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Controlla la modalità di visualizzazione del riquadro di anteprima.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la proprietà di stile corrente per il riquadro di anteprima.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





