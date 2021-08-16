---
title: Proprietà DisplayName IResultProperty (WdsSharedIDL.h)
description: Nome visualizzato localizzato della proprietà.
ms.assetid: 8f9e118a-9e92-4919-afe1-735c61af38f7
keywords:
- Proprietà DisplayName Funzionalità dell'Windows legacy
- Proprietà DisplayName Legacy Windows Environment Features , interfaccia IResultProperty
- Interfaccia IResultProperty Legacy Windows funzionalità dell'ambiente, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultProperty.DisplayName
- IResultProperty.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e15eedcafffbae25b2671b02aaac8fd1e64b625edfea3e040ed2c6067ca953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755163"
---
# <a name="iresultpropertydisplayname-property"></a>Proprietà IResultProperty::D isplayName

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Nome visualizzato localizzato della proprietà.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

restituisce un puntatore al nome visualizzato localizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





