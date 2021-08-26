---
title: Proprietà IResultVerb Enabled (WdsSharedIDL.h)
description: Questa proprietà restituisce TRUE se il verbo è abilitato.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Proprietà Enabled Funzionalità dell'ambiente Windows legacy
- Proprietà Enabled Legacy Windows Environment Features , interfaccia IResultVerb
- Interfaccia IResultVerb Legacy Windows Environment Features , proprietà Enabled
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
ms.openlocfilehash: c96a4c40252bf6b5ab74d3d4ec96e2568dffeed624ae2b5126059192dd72d9e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014321"
---
# <a name="iresultverbenabled-property"></a>Proprietà IResultVerb::Enabled

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Questa proprietà restituisce TRUE se il verbo è abilitato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà restituisce True se il verbo è abilitato o False in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 con SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

 





