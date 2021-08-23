---
title: Gestione degli errori sconosciuti
description: Gestione degli errori sconosciuti
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fb0e8aaaef8fc3ff4ae9bb76f76a845c325c4b5a5dc4d409dbd0ab35734ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048259"
---
# <a name="handling-unknown-errors"></a>Gestione degli errori sconosciuti

È legale restituire un codice di stato solo dall'implementazione di un metodo di interfaccia sancito come legalmente restituibile. La mancata osservazione di questa regola consente di creare un conflitto tra i valori del codice di errore restituiti e quelli sanzionati dall'applicazione. Prestare particolare attenzione a questo potenziale problema quando si propagano codici di errore da funzioni chiamate internamente.

Le applicazioni che chiamano le interfacce devono considerare qualsiasi codice di errore restituito sconosciuto (anziché un codice di esito positivo) come sinonimo di E \_ UNEXPECTED. Questa pratica di gestione dei codici di errore sconosciuti è richiesta dai client delle funzioni e delle interfacce definite da COM. Poiché la tipica procedura di programmazione consiste nel gestire alcuni codici di errore specifici in modo dettagliato e nel trattare il resto in modo generico, questo requisito di gestione dei codici di errore imprevisti o sconosciuti è facilmente soddisfatto.

È importante gestire tutti gli errori possibili quando si chiama un metodo di interfaccia. In caso contrario, l'applicazione potrebbe bloccarsi, danneggiare i dati o diventare vulnerabile agli exploit di sicurezza. L'esempio di codice seguente illustra il modo consigliato per gestire gli errori sconosciuti:


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



Il controllo degli errori seguente viene spesso usato con le routine che non restituiscono alcun elemento speciale ,ad eccezione di S \_ OK o di un errore imprevisto:


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

 

 




