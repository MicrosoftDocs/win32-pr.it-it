---
title: Proprietà DisplayName IResultType (WdsSharedIDL. h)
description: Nome visualizzato localizzato del tipo
ms.assetid: 21695ba3-aa6d-419b-961a-0643caa5ea1f
keywords:
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy
- Proprietà DisplayName caratteristiche dell'ambiente Windows legacy, interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, proprietà DisplayName
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
ms.openlocfilehash: 94080a2b5c6121bbaa9b611a7d55c2d5aaeed5e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301414"
---
# <a name="iresulttypedisplayname-property"></a>IResultType::D proprietà di riproduzione

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Nome visualizzato localizzato del tipo:

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a>Valore proprietà

Restituisce l'indirizzo del nome visualizzato localizzato per il tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





