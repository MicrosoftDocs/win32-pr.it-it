---
title: Proprietà DisplayName IResultType (WdsSharedIDL.h)
description: Nome visualizzato localizzato del tipo
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Proprietà DisplayName Funzionalità dell'Windows legacy
- Proprietà DisplayName Legacy Windows Environment Features , interfaccia IResultType
- Interfaccia IResultType legacy Windows funzionalità dell'ambiente, proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultType.DisplayName
- IResultType.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e045306250d2642ae281d81c8ffb8ab5a298134bf999ddba6abd5fd1660aeb1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399787"
---
# <a name="iresulttypedisplayname-property"></a>Proprietà IResultType::D isplayName

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Nome visualizzato localizzato del tipo:

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

restituisce l'indirizzo del nome visualizzato localizzato per il tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





