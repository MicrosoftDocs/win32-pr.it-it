---
description: La classe CCritSec fornisce un blocco thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Classe CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326829"
---
# <a name="ccritsec-class"></a>Classe CCritSec

La classe **CCritSec** fornisce un blocco thread.

Questa classe è un wrapper sottile per un oggetto **\_ sezione critica** di Windows. È possibile bloccare e sbloccare il thread chiamando il metodo [**CCritSec:: Lock**](ccritsec-lock.md) e [**CCritSec:: Unlock**](ccritsec-unlock.md) . Tuttavia, è più sicuro usare questa classe insieme alla classe [**CAutoLock**](cautolock.md) . Quando la classe **CAutoLock** esce dall'ambito, sblocca automaticamente l'oggetto **CCritSec** . Inoltre, viene compilato in codice inline efficiente.



| Variabili membro pubblico                            | Descrizione                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**\_currentOwner m**](ccritsec-m-currentowner.md) | Identificatore del thread proprietario.                  |
| [**\_lockCount m**](ccritsec-m-lockcount.md)       | Numero di blocchi in attesa su questo oggetto.              |
| [**\_fTrace m**](ccritsec-m-ftrace.md)             | Valore booleano che specifica se tracciare il blocco. |
| Metodi pubblici                                     | Descrizione                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Metodo del costruttore.                                      |
| [**~ CCritSec**](ccritsec--ccritsec.md)            | Metodo del distruttore.                                       |
| [**Lock**](ccritsec-lock.md)                      | Blocca l'oggetto sezione critica.                       |
| [**Sblocca**](ccritsec-unlock.md)                  | Sblocca l'oggetto sezione critica.                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti sezione critica](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[Riferimento alla classe base DirectShow](base-class-reference.md)
</dt> </dl>

 

