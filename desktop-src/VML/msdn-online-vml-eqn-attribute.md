---
title: Attributo VML Eqn
description: Attributo VML Eqn
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae5872c29064f24a10b4a12c0d0e2a4ca4a200f79e295d60713fe56355f23aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655451"
---
# <a name="vml-eqn-attribute"></a>Attributo VML Eqn

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce l'equazione usata da una formula. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[F](msdn-online-vml-f-element.md) (sottoelemento [di formule](msdn-online-vml-formulas-element.md))

**Sintassi dei tag**

<v: *elemento* eqn=" *espressione* ">

**Sintassi dello script**

*element* .eqn="*expression*"

*expression* = *elemento*.eqn

**Osservazioni:**

Le equazioni sono definite dalla valutazione di un'espressione di testo con la forma generale di un'operazione seguita da un massimo di tre argomenti. Ogni argomento può essere dei tipi seguenti:

-   rettifica (ad esempio, \# 2)
-   un'altra formula (ad esempio, @2 )
-   numeri fissi (ad esempio, 2)
-   valori predefiniti

La tabella seguente definisce le formule che possono essere usate con gli argomenti facoltativi dati i nomi *v*, *p1* e *p2*. Il modello di formula è:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Operazione | Parametri | Exact  | Risultato                    | Descrizione                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | sì    | v                         | Definisce un valore guida da un altro valore.                                   |
| Sum       | 3      | sì    | v + p1 - p2               | Usato per l'addizione e la sottrazione.                                             |
| product   | 3      | Giri | v \* p1/p2              | Usato per la moltiplicazione e la divisione.                                          |
| mid       | 2      | (c)    | (v + p1)/ 2               | Nella media.                                                                       |
| abs       | 1      | sì    | abs(v)                    | Valore assoluto.                                                                |
| min       | 2      | sì    | min(v,p1)                 | Valore minore di v e p1.                                                  |
| max       | 2      | sì    | max(v,p1)                 | Valore maggiore di v e p1.                                                 |
| if        | 3      | sì    | v > 0 ? p1 : p2        | Test condizionale.                                                           |
| mod       | 3      | no     | sqrt(v^2 + p1^2 + p2^2)   | Valore modulo.                                                                 |
| atan2     | 2      | no     | atan2(p1,v)               | Valore polare in \* gradi 2^16 (unità fd).                                     |
| sin       | 2      | no     | v \* sin(p1)              | Sin, argomento in gradi \* 2^16 (unità fd ). [](msdn-online-vml-units.md)     |
| cos       | 2      | no     | v \* cos(p1)              | Cos, argomento in gradi \* 2^16 (unità fd ). [](msdn-online-vml-units.md)     |
| cosatan2  | 3      | no     | v \* cos(atan2(p2,p1))    | Mantiene l'accuratezza completa nel calcolo intermedio.                           |
| sinatan2  | 3      | no     | v \* sin(atan2(p2,p1))    | Mantiene l'accuratezza completa nel calcolo intermedio.                           |
| sqrt      | 1      | no     | sqrt(v)                   | Il risultato è positivo e viene arrotondato per e per intero.                                            |
| sumangle  | 3      | sì    | v + p1 \* 2^16 + p2 \* 2^16 | v ridimensionato di 2^16; p1 e p2 sono gradi.<br/>                            |
| ellipse   | 3      | no     | p2 \* sqrt(1-(v/p1)^2)    | Ellisse.                                                                       |
| tan       | 2      | no     | v \* tan(p1)              | Tangente, argomento in gradi \* 2^16 (unità fd ). [](msdn-online-vml-units.md) |



 

Si noti che l'equazione è costituita solo da operazioni e numeri. I simboli matematici vengono omessi. Ad esempio, l'equazione

eqn="sum 5 9 3"

produrrebbe l'equivalente di

5 + 9 - 3

per il valore restituito di 11. Se gli operandi non sono presenti, il valore non viene usato. Ad esempio,

eqn="sum 5 9"

produrrebbe l'equivalente di

5 + 9

e ignorano l'operando mancante.

*Attributo standard VML*

**Esempio**

La formula seguente restituisce un risultato di 6 (somma di entrambi i numeri divisi per 2), che, se si tratta della prima formula, può essere recuperata dal simbolo " @0 ".


```HTML
    <v:f eqn="mid 5 7"/>
```



 

