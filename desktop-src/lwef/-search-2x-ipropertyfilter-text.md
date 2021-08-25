---
title: Proprietà Text IPropertyFilter (WdsSharedIDL.h)
description: Testo del filtro.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Proprietà Text Funzionalità dell'ambiente Windows legacy
- Proprietà Text Legacy Windows Environment Features , interfaccia IPropertyFilter
- Interfaccia IPropertyFilter Legacy Windows funzionalità dell'ambiente, proprietà Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5dd572fe2edf82b2e882b73e2aec772090afda791117b0c1ac2fb14b115f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963801"
---
# <a name="ipropertyfiltertext-property"></a>Proprietà IPropertyFilter::Text

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Testo del filtro.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a>Valore proprietà

Imposta il testo del filtro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





