---
title: Proprietà IResultsViewer PreviewStyle (WdsView.h)
description: Controlla la modalità di visualizzazione del riquadro di anteprima.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- Proprietà PreviewStyle Funzionalità dell'ambiente Windows legacy
- Proprietà PreviewStyle Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer Legacy Windows dell'ambiente, proprietà PreviewStyle
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
ms.openlocfilehash: b412c92ca82263481b83ce739d44f21c2d15d99e9e6e7c74502480e0d8fad1b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753783"
---
# <a name="iresultsviewerpreviewstyle-property"></a>Proprietà IResultsViewer::P reviewStyle

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

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
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





