---
description: Valore booleano che specifica se tracciare il blocco.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Membro CCritSec:: m_fTrace (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332646"
---
# <a name="ccritsecm_ftrace-member"></a>Membro fTrace di CCritSec:: m \_

Valore booleano che specifica se tracciare il blocco.

## <a name="syntax"></a>Sintassi


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a>Osservazioni

Questa variabile membro viene definita solo nella versione di debug della classe di base. Se il valore è **true**, una traccia dello stato di blocco viene scritta nel log di debug. (È necessario che la registrazione di debug per le sezioni critiche sia attiva). Per ulteriori informazioni, vedere [**DbgLockTrace**](dbglocktrace.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCritSec**](ccritsec.md)
</dt> </dl>

 

 




