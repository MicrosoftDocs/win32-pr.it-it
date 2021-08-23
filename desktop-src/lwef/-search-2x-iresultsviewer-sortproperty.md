---
title: Proprietà SortProperty IResultsViewer (WdsView.h)
description: Questa proprietà imposta o restituisce l'oggetto IndexColumn della proprietà in base al quale ordinare i risultati.
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- Proprietà SortProperty Funzionalità dell'Windows legacy
- Proprietà SortProperty Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer Legacy Windows Environment Features , proprietà SortProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ab912dde6bdc87b2e9d05496f25de497b6fdc9c8fde4e65e3d2cb89549b1e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610931"
---
# <a name="iresultsviewersortproperty-property"></a>Proprietà IResultsViewer::SortProperty

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà imposta o restituisce l'oggetto IndexColumn della proprietà in base al quale ordinare i risultati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la proprietà IndexColumn.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





