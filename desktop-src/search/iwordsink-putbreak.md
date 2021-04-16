---
description: Inserisce un'interruzioni dopo la parola precedente.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: Metodo IWordSink::P utBreak (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342931"
---
# <a name="iwordsinkputbreak-method"></a>IWordSink::P metodo utBreak

Inserisce un'interruzioni dopo la parola precedente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*breakType* \[ in\]
</dt> <dd>

Valore del [**\_ \_ tipo di WORDREP break**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) che indica il tipo di interruzioni inserite dal WordSink dopo la parola precedente. Ogni break occupa una posizione univoca nell'indice. Pertanto, l'inserimento di interruzioni tra le parole cambia la distanza relativa tra le parole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | L'operazione è stata completata correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I metodi [**IWordSinkPutWord**](iwordsink-putword.md) e [**IWordSink::P utaltword**](iwordsink-putaltword.md) inseriscono automaticamente un'interruzioni di fine della parola (EOW, indicata dall' \_ elemento WORDREP break \_ EOW del tipo enumerato [**WORDREP \_ \_ break**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) dopo ogni parola. Chiamare il metodo **PutBreak** per inserire un tipo di interruzioni diverso dalla fine della parola. Questo metodo non modifica il buffer del testo di origine (*pSourceText*) o incrementa il numero di caratteri (*CWC*). Tuttavia, incrementa la posizione corrente nell'indice e influiscono sui risultati della query.

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

 

 
