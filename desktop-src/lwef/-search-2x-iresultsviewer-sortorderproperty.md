---
title: Proprietà IResultsViewer::SortOrderProperty (WdsView.h)
description: Questa proprietà consente di impostare o restituire l'ordine delle colonne in base a cui ordinare i risultati.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà SortOrderProperty
- Proprietà SortOrderProperty caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà SortOrderProperty
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
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301542"
---
# <a name="iresultsviewersortorderproperty-property"></a>Proprietà IResultsViewer:: SortOrderProperty

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà consente di impostare o restituire l'ordine delle colonne in base a cui ordinare i risultati.

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

Imposta la proprietà [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





