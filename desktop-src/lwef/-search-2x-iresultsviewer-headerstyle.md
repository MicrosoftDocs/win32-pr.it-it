---
title: Proprietà IResultsViewer HeaderStyle (WdsView.h)
description: Stile dell'intestazione visualizzata nella visualizzazione.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- Proprietà HeaderStyle Funzionalità dell'Windows legacy
- Proprietà HeaderStyle Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer Legacy Windows Environment Features , proprietà HeaderStyle
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
ms.openlocfilehash: 6c7c60687c3d306c3f9c3fcbb551f2d746723c7223b1964d42386464729b4069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753892"
---
# <a name="iresultsviewerheaderstyle-property"></a>Proprietà IResultsViewer::HeaderStyle

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

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
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





