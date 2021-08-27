---
title: Proprietà DisplayName IResultsViewer (WdsView.h)
description: Nome visualizzato localizzato del tipo.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Proprietà DisplayName Funzionalità dell'Windows legacy
- Proprietà DisplayName Legacy Windows Environment Features , interfaccia IResultsViewer
- Interfaccia IResultsViewer legacy Windows funzionalità dell'ambiente, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98d3f0c5f7887861d2d757c71a4327ce57af7f39ae3f4811167789c6b4e662ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754396"
---
# <a name="iresultsviewerdisplayname-property"></a>Proprietà IResultsViewer::D isplayName

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Nome visualizzato localizzato del tipo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un valore che riceve il nome visualizzato localizzato per il tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                 |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                        |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>WdsView.h</dt> </dl> |



 

 





