---
description: La proprietà del linguaggio di sola lettura dell'oggetto Error restituisce il LANGID dell'errore corrente.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Proprietà Error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329750"
---
# <a name="errorlanguage-property"></a>Proprietà Error. Language

La proprietà del **linguaggio** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce il **LangID** dell'errore corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Il valore della proprietà **Language** è-1, a meno che l'errore non sia di tipo MsmErrorLanguageUnsupported o msmErrorLanguageFailed. È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .

### <a name="c"></a>C++

Vedere [**get \_ Language function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

