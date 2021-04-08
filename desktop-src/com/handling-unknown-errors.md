---
title: Gestione degli errori sconosciuti
description: Gestione degli errori sconosciuti
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045277"
---
# <a name="handling-unknown-errors"></a>Gestione degli errori sconosciuti

È lecito restituire un codice di stato solo dall'implementazione di un metodo di interfaccia approvato come legalmente restituibile. La mancata osservanza di questa regola consente di verificare la possibilità di conflitto tra i valori restituiti del codice di errore e quelli approvati dall'applicazione. Prestare particolare attenzione a questo potenziale problema durante la propagazione dei codici di errore dalle funzioni chiamate internamente.

Le applicazioni che chiamano interfacce devono considerare qualsiasi codice di errore restituito sconosciuto (in contrapposizione a un codice di esito positivo) come sinonimo di E \_ imprevisto. Questa pratica di gestione dei codici di errore sconosciuti è richiesta dai client delle funzioni e delle interfacce definite da COM. Poiché la procedura di programmazione tipica consiste nel gestire alcuni codici di errore specifici e trattare il resto in modo generico, è facile soddisfare questo requisito per la gestione di codici di errore imprevisti o sconosciuti.

È importante gestire tutti i possibili errori quando si chiama un metodo di interfaccia. In caso contrario, potrebbe causare l'arresto anomalo dell'applicazione, il danneggiamento dei dati o il rischio di essere vulnerabile agli exploit di sicurezza. Nell'esempio di codice seguente viene illustrata la modalità consigliata per la gestione degli errori sconosciuti:


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



Il controllo degli errori seguente viene spesso usato con le routine che non restituiscono alcun valore speciale (ad eccezione di S \_ OK o di un errore imprevisto):


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori in COM](error-handling-in-com.md)
</dt> </dl>

 

 




