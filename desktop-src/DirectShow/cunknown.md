---
description: La classe CUnknown implementa l'interfaccia IUnknown. La maggior parte degli oggetti Component Object Model (COM) in DirectShow derivano da CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Classe CUnknown (ComBase. h)
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
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331444"
---
# <a name="cunknown-class"></a>Classe CUnknown

![gerarchia di classi CUnknown](images/cbase01.png)

La classe **CUnknown** implementa l'interfaccia **IUnknown** . La maggior parte degli oggetti Component Object Model (COM) in DirectShow derivano da **CUnknown**.

Se si implementa un oggetto COM, potrebbe essere necessario derivarlo da **CUnknown**. La derivazione da **CUnknown** fornisce un'implementazione thread-safe e consente di evitare il problema di implementare **IUnknown**.

Per una descrizione dettagliata di come usare questa classe di base, vedere [How to implement IUnknown](how-to-implement-iunknown.md). Di seguito è riportato un breve riepilogo:

-   Includere la macro [**Declare \_ IUnknown**](declare-iunknown.md) nella sezione public della definizione della classe. Questa macro dichiara i tre metodi dell'interfaccia **IUnknown** .
-   Eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per supportare interfacce diverse da **IUnknown**. All'interno di questo metodo, chiamare la funzione [**GetInterface**](getinterface.md) per recuperare i puntatori di interfaccia.
-   Nel costruttore della classe richiamare il metodo del costruttore **CUnknown** .



| Variabili membro protette                                                  | Descrizione                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**\_cref m**](cunknown-m-cref.md)                                          | Conteggio riferimenti.                                                   |
| Metodi pubblici                                                              | Descrizione                                                        |
| [**CUnknown**](cunknown-cunknown.md)                                       | Metodo del costruttore.                                                |
| [**~ CUnknown**](cunknown--cunknown.md)                                    | Metodo del distruttore. Virtuale.                                        |
| [**GetOwner**](cunknown-getowner.md)                                       | Ottiene un puntatore all' **IUnknown** di controllo.                    |
| Metodi INonDelegatingUnknown                                               | Descrizione                                                        |
| [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md)                 | Incrementa il conteggio dei riferimenti.                                    |
| [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) | Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti. |
| [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md)               | Decrementa il conteggio dei riferimenti.                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi base di DirectShow](directshow-base-classes.md)
</dt> </dl>

 

 




