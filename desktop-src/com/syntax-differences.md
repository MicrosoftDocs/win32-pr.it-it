---
title: Differenze di sintassi
description: La modifica più evidente quando ci si sposta tra linguaggi di programmazione è la modifica della sintassi.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef58f92bf87d877c2c55a73fe5f717b93c359119e5ca6aa73fc1aeee531d858
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678391"
---
# <a name="syntax-differences"></a>Differenze di sintassi

La modifica più evidente quando ci si sposta tra linguaggi di programmazione è la modifica della sintassi.

Si consideri il metodo Add dell'oggetto EnhEvents, mostrato come dichiarato in tre linguaggi diversi.

``` syntax
object.Add(Time As Double, Name As String) As Variant

HRESULT Add(
  double Time, 
  BSTR Name, 
  VARIANT* pVal
);
 
public com.ms.com.Variant Add( 
  double Time, 
  java.lang.String Name
);
 
```

Anche se la sintassi di ogni linguaggio esprime il metodo in modo diverso, la funzionalità è la stessa. In ogni lingua, il metodo Add accetta i parametri *Time* e *Name* e restituisce un oggetto EnhEvent. Nell'esempio di C++ il metodo restituisce l'oggetto usando un terzo parametro di output, *pVal.*

In genere, la funzionalità di un oggetto COM è la stessa in tutti i linguaggi di programmazione. Per questo, la documentazione per un oggetto COM è utile anche se l'oggetto è documentato in un altro linguaggio di programmazione rispetto a quello in uso. Le descrizioni delle funzionalità, dei parametri e dei valori restituiti dell'oggetto sono, con poche eccezioni, valide per tutti i linguaggi.

Per informazioni su come convertire la sintassi di un oggetto COM in un altro linguaggio di programmazione, vedere Conversione della [sintassi](translating-com-object-syntax-for-programming-languages.md)degli oggetti COM per i linguaggi di programmazione .

Le differenze di sintassi tra i linguaggi di scripting JavaScript, JScript e VBScript sono meno pronunciate rispetto alle differenze di sintassi tra i linguaggi di programmazione illustrati in precedenza. Si consideri ad esempio la funzione quadrata implementata in ognuno di questi tre linguaggi di scripting:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Si noti che i linguaggi di scripting, a differenza dei linguaggi di programmazione, sono tipi di dati deboli. In altre parole, non è necessario specificare il tipo di dati di un parametro o di un valore restituito quando si dichiara una funzione. Viene invece eseguito automaticamente il cast delle variabili al tipo di dati appropriato. Nel caso di VBScript, tutte le variabili sono dello stesso tipo di dati, **Variant.**

La sintassi JavaScript e JScript per square è la stessa. JScript è in gran parte compatibile con JavaScript. Tuttavia, JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio **ActiveXObject**, **Enumerator,** **Error,** **Global** e **VBArray.** Per altre informazioni su questi oggetti, vedere le informazioni di [riferimento JScript linguaggio.](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100))

In superficie, la sintassi JavaScript e JScript è simile alla sintassi Java. Questa somiglianza è solo superficiale. Il linguaggio Java è stato sviluppato indipendentemente da JavaScript e JScript e non è correlato a nessuno dei due.

VBScript, d'altra parte, è un subset del linguaggio Visual Basic programmazione. Per questo, la sintassi VBScript è un subset Visual Basic sintassi ed è spesso intercambiabile con Visual Basic sintassi.

Per informazioni sull'uso di oggetti COM nei linguaggi di scripting, vedere [Scripting con oggetti COM.](scripting-with-com-objects.md)

 

 