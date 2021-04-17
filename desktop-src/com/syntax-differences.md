---
title: Differenze di sintassi
description: Il cambiamento più evidente quando ci si sposta tra i linguaggi di programmazione è la modifica della sintassi.
ms.assetid: 179efb69-3794-4a06-b770-2b3dc8409172
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d3a9c2123d8b94f9fc6fe79d4ab48188830c7a1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474350"
---
# <a name="syntax-differences"></a>Differenze di sintassi

Il cambiamento più evidente quando ci si sposta tra i linguaggi di programmazione è la modifica della sintassi.

Si consideri il metodo Add dell'oggetto EnhEvents, illustrato come viene dichiarato in tre lingue diverse.

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

Sebbene la sintassi di ogni linguaggio esprima il metodo in modo diverso, la funzionalità è la stessa. In ogni linguaggio, il metodo Add accetta i parametri *Time* e *Name* e restituisce un oggetto EnhEvent. Nell'esempio di C++, il metodo restituisce l'oggetto usando un terzo parametro di output, *pval*.

In genere, la funzionalità di un oggetto COM è la stessa in tutti i linguaggi di programmazione. Per questo motivo, la documentazione relativa a un oggetto COM è utile anche se l'oggetto è documentato in un altro linguaggio di programmazione rispetto a quello in uso. Le descrizioni delle funzionalità, dei parametri e dei valori restituiti dell'oggetto sono, con poche eccezioni, valide per tutti i linguaggi.

Per informazioni su come convertire la sintassi di un oggetto COM in un altro linguaggio di programmazione, vedere [traduzione della sintassi degli oggetti com per i linguaggi di programmazione](translating-com-object-syntax-for-programming-languages.md).

Le differenze di sintassi tra i linguaggi di scripting JavaScript, JScript e VBScript sono meno evidenti rispetto alle differenze di sintassi tra i linguaggi di programmazione illustrati in precedenza. Si consideri, ad esempio, la funzione quadrata implementata in ognuno di questi tre linguaggi di scripting:

``` syntax
Function square(x)
  square = x*x
End Function
 
function square(x){ return x*x; }
 
function square(x){ return x*x; }
 
```

Si noti che i linguaggi di scripting, a differenza dei linguaggi di programmazione, sono debolmente tipizzati. In altre parole, non è necessario specificare il tipo di dati di un parametro o di un valore restituito quando si dichiara una funzione. Al contrario, viene eseguito automaticamente il cast delle variabili al tipo di dati appropriato. Nel caso di VBScript, tutte le variabili hanno lo stesso tipo di dati, **Variant**.

La sintassi JavaScript e JScript per Square è la stessa. JScript è ampiamente compatibile con JavaScript. Tuttavia, JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio **ActiveXObject**, **Enumerator**, **Error**, **Global** e **VBArray**. Per ulteriori informazioni su questi oggetti, vedere la Guida di [riferimento al linguaggio JScript](/previous-versions/visualstudio/visual-studio-2010/ye921ye4(v=vs.100)).

Sulla superficie, la sintassi di JavaScript e JScript è simile alla sintassi Java. Questa somiglianza è solo superficiale. Il linguaggio Java è stato sviluppato indipendentemente da JavaScript e JScript e non è correlato a entrambi.

VBScript, d'altra parte, è un subset del linguaggio di programmazione Visual Basic. Per questo motivo, la sintassi VBScript è un subset della sintassi Visual Basic e spesso è interscambiabile con Visual Basic sintassi.

Per informazioni sull'utilizzo di oggetti COM in linguaggi di scripting, vedere Creazione di [script con oggetti com](scripting-with-com-objects.md).

 

 