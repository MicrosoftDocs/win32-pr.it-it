---
description: La classe CCritSec fornisce un blocco del thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Classe CCritSec (Wxutil.h)
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
ms.openlocfilehash: eb57004935a85392057120c0ec369d19217148780079ab4be83088dd3de3ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872191"
---
# <a name="ccritsec-class"></a>Classe CCritSec

La **classe CCritSec** fornisce un blocco del thread.

Questa classe è un thin wrapper per un Windows **CRITICAL \_ SECTION.** È possibile bloccare e sbloccare il thread chiamando i metodi [**CCritSec::Lock**](ccritsec-lock.md) e [**CCritSec::Unlock.**](ccritsec-unlock.md) Tuttavia, è più sicuro usare questa classe in combinazione con la [**classe CAutoLock.**](cautolock.md) Quando la **classe CAutoLock** esce dall'ambito, sblocca automaticamente **l'oggetto CCritSec.** Inoltre, viene compilato in codice inline efficiente.



| Variabili membro pubbliche                            | Descrizione                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentOwner**](ccritsec-m-currentowner.md) | Identificatore di thread del thread proprietario.                  |
| [**m \_ lockCount**](ccritsec-m-lockcount.md)       | Numero di blocchi in sospeso su questo oggetto.              |
| [**m \_ fTrace**](ccritsec-m-ftrace.md)             | Valore booleano che specifica se tracciare questo blocco. |
| Metodi pubblici                                     | Descrizione                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | Metodo del costruttore.                                      |
| [**~CCritSec**](ccritsec--ccritsec.md)            | Metodo del distruttore.                                       |
| [**Lock**](ccritsec-lock.md)                      | Blocca l'oggetto sezione critica.                       |
| [**Sblocca**](ccritsec-unlock.md)                  | Sblocca l'oggetto sezione critica.                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti sezione critica](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[DirectShow Informazioni di riferimento sulla classe base](base-class-reference.md)
</dt> </dl>

 

