---
title: Proprietà IResultsViewer::SortOrderProperty (WdsView.h)
description: Questa proprietà imposta o restituisce l'ordine delle colonne in base alle quali ordinare i risultati.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Proprietà SortOrderProperty Funzionalità legacy Windows'ambiente
- Proprietà SortOrderProperty Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer legacy Windows dell'ambiente, proprietà SortOrderProperty
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01680ac46592887cf4f321b771ff0e46039c775c4e9e9d8ed1edbc893ab45977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829171"
---
# <a name="iresultsviewersortorderproperty-property"></a>Proprietà IResultsViewer::SortOrderProperty

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà imposta o restituisce l'ordine delle colonne in base alle quali ordinare i risultati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a>Valore proprietà

Imposta la [**proprietà ColumnSortOrder.**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





