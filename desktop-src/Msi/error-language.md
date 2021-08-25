---
description: La proprietà Language di sola lettura dell'oggetto Error restituisce il LANGID dell'errore corrente.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Proprietà Error.Language (Mergemod.h)
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
ms.openlocfilehash: 966725be2378292215ffaad6c7fc96fb36fd305d2bb2b6053849816dd1fb3f70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082891"
---
# <a name="errorlanguage-property"></a>Error.Language - proprietà

La proprietà **Language** di sola lettura [**dell'oggetto Error**](error-object.md) restituisce il **LANGID** dell'errore corrente.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Error.Language
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Il valore della proprietà **Language** è -1 a meno che l'errore non sia di tipo msmErrorLanguageUnsupported o msmErrorLanguageFailed. È possibile determinare il tipo di errore chiamando la [**proprietà Type**](error-type.md) dell'oggetto [**Error.**](error-object.md)

### <a name="c"></a>C++

Vedere [**get Language Function \_ (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

