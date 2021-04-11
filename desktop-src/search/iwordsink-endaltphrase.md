---
description: Indica la fine della frase finale in una sequenza di frasi alternative generate da un Word breaker in fase di indicizzazione.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Metodo IWordSink:: EndAltPhrase (search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225942"
---
# <a name="iwordsinkendaltphrase-method"></a>Metodo IWordSink:: EndAltPhrase

Indica la fine della frase finale in una sequenza di frasi alternative generate da un Word breaker in fase di indicizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                           | Descrizione                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ solo query WBREAK \_ E**</dt> </dl> | [**EndAltPhrase**](iwordsink-endaltphrase.md) viene chiamato durante la fase di query.<br/> |



 

## <a name="remarks"></a>Commenti

Le implementazioni [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) chiamano **IWordSink:: EndAltPhrase** dal metodo [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) per terminare una sequenza di frasi alternative. Il metodo [**IWordSink:: StartAltPhrase**](iwordsink-startaltphrase.md) viene chiamato per indicare la fine di una frase e l'inizio di un altro oggetto in una sequenza di frasi. Solo l'ultima frase in una sequenza viene terminata con una chiamata a **EndAltPhrase**.

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

 

 
