---
title: Proprietà Enabled di IResultVerb (WdsSharedIDL. h)
description: Questa proprietà restituisce TRUE se il verbo è abilitato.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Funzionalità della proprietà Enabled ambiente Windows legacy
- Funzionalità abilitate proprietà ambiente Windows legacy, interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, proprietà Enabled
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964492"
---
# <a name="iresultverbenabled-property"></a>Proprietà IResultVerb:: Enabled

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Questa proprietà restituisce TRUE se il verbo è abilitato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà restituisce true se il verbo è abilitato o false in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





