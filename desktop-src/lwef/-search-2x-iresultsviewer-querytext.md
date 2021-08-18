---
title: Proprietà QueryText IResultsViewer (WdsView.h)
description: Ottiene o imposta il testo della query corrente.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Proprietà QueryText Funzionalità dell'Windows legacy
- Proprietà QueryText Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer Legacy Windows Environment Features , proprietà QueryText
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5522419d14bf27a1e836c9caa16e9dabf5a122e4566fd19c868a1f72e3f61d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753586"
---
# <a name="iresultsviewerquerytext-property"></a>Proprietà IResultsViewer::QueryText

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Ottiene o imposta il testo della query corrente.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il testo della query corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





