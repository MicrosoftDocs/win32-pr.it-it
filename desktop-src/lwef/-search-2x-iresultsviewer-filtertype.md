---
title: Proprietà IResultsViewer FilterType (WdsView.h)
description: Questa proprietà imposta o restituisce il nome del tipo pre-percepito in base a cui filtrare i risultati.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- Proprietà FilterType Funzionalità dell'Windows legacy
- Proprietà FilterType Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer Legacy Windows ambiente, proprietà FilterType
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8f4e71a469ad68431721d99343b43b28ea0f0a82b7e393f5c402b0d88735db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754307"
---
# <a name="iresultsviewerfiltertype-property"></a>Proprietà IResultsViewer::FilterType

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà imposta o restituisce il nome del tipo pre-percepito in base a cui filtrare i risultati.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il tipo percepito usato per filtrare i risultati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





