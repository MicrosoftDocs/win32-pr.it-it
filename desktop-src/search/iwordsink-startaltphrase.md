---
description: Indica il limite tra le frasi in una sequenza di frasi alternative generate da un Word breaker durante l'esecuzione dell'indice.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Metodo IWordSink:: StartAltPhrase (search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225941"
---
# <a name="iwordsinkstartaltphrase-method"></a>Metodo IWordSink:: StartAltPhrase

Indica il limite tra le frasi in una sequenza di frasi alternative generate da un Word breaker durante l'esecuzione dell'indice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                           | Descrizione                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ solo query WBREAK \_ E**</dt> </dl> | [**StartAltPhrase**](iwordsink-startaltphrase.md) viene chiamato durante la fase di query.<br/> |



 

## <a name="remarks"></a>Commenti

Ogni frase alternativa inizia con una chiamata **StartAltPhrase** . La frase viene inserita nell'oggetto [**IWordSink**](iwordsink.md) tramite chiamate successive al metodo [**IWordSink::P utword**](iwordsink-putword.md) o [**IWordSink::P utaltword**](iwordsink-putaltword.md) . La frase alternativa finale in una sequenza di frasi viene terminata con una chiamata al metodo [**IWordSink:: EndAltPhrase**](iwordsink-endaltphrase.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Search. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 




