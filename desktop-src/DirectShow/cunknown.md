---
description: La classe CUnknown implementa l'interfaccia IUnknown. La maggior Component Object Model (COM) in DirectShow deriva da CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Classe CUnknown (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b6089f7f1c108a9b99ad4f1b16f4638b84d8d687a3590353c32841ccfff499
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075997"
---
# <a name="cunknown-class"></a>Classe CUnknown

![Gerarchia di classi cunknown](images/cbase01.png)

La **classe CUnknown** implementa **l'interfaccia IUnknown.** La maggior Component Object Model (COM) in DirectShow deriva da **CUnknown.**

Se si implementa un oggetto COM, è possibile derivarlo da **CUnknown.** La derivazione **da CUnknown** fornisce un'implementazione thread-safe e consente di risparmiare i problemi di implementazione **di IUnknown.**

Per una descrizione dettagliata dell'uso di questa classe di base, vedere [Come implementare IUnknown.](how-to-implement-iunknown.md) Di seguito è riportato un breve riepilogo:

-   Includere la macro [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) nella sezione pubblica della definizione di classe. Questa macro dichiara i tre metodi **dell'interfaccia IUnknown.**
-   Eseguire [**l'override del metodo NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per supportare interfacce diverse **da IUnknown.** All'interno di questo metodo chiamare la [**funzione GetInterface**](getinterface.md) per recuperare i puntatori a interfaccia.
-   Nel costruttore della classe richiamare il **metodo del costruttore CUnknown.**



| Variabili membro protette                                                  | Descrizione                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**m \_ cRef**](cunknown-m-cref.md)                                          | Conteggio dei riferimenti.                                                   |
| Metodi pubblici                                                              | Descrizione                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Metodo del costruttore.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Metodo del distruttore. Virtuale.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Ottiene un puntatore all'oggetto **IUnknown di controllo.**                    |
| Metodi INonDelegatingUnknown                                               | Descrizione                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Incrementa il conteggio dei riferimenti.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Decrementa il conteggio dei riferimenti.                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Classi di base](directshow-base-classes.md)
</dt> </dl>

 

 




