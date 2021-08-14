---
title: Proprietà DisplayName IResultVerb (WdsSharedIDL.h)
description: Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Proprietà DisplayName Funzionalità dell'Windows legacy
- Proprietà DisplayName Legacy Windows Environment Features , interfaccia IResultVerb
- Interfaccia IResultVerb Legacy Windows Environment Features , proprietà DisplayName
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d7f72d0d028fa6a6ecdede7f2d88e3e3dea0a37a14cc6365dc5da2d14992af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117694719"
---
# <a name="iresultverbdisplayname-property"></a>Proprietà IResultVerb::D isplayName

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





