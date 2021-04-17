---
title: Proprietà IResultsViewer itemStore sconosciuta (WdsView. h)
description: Questa proprietà consente di impostare o restituire il nome dell'archivio in base al quale filtrare i risultati.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Funzionalità dell'ambiente Windows legacy della proprietà itemStore sconosciuta
- Proprietà itemStore sconosciuta caratteristiche dell'ambiente Windows legacy, interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, proprietà itemStore sconosciuta
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476505"
---
# <a name="iresultsvieweritemstore-property"></a>Proprietà IResultsViewer:: itemStore sconosciuta

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà consente di impostare o restituire il nome dell'archivio in base al quale filtrare i risultati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

Imposta i nomi dell'archivio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView. h</dt> </dl> |



 

 





