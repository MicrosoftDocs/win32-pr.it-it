---
title: Attributo EQN di la
description: Attributo EQN di la
ms.assetid: b2c41bad-2f83-4280-9441-33206d8dc1b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da00084a825147c6f8a05f503e5ee2679f40e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339182"
---
# <a name="vml-eqn-attribute"></a>Attributo EQN di la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Definisce l'equazione utilizzata da una formula. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[F](msdn-online-vml-f-element.md) (sottoelemento delle [formule](msdn-online-vml-formulas-element.md))

**Sintassi Tag**

<v: *element* EQN = " *Expression* " >

**Sintassi dello script**

*element* . eqn = "*Expression*"

*espressione* = *elemento*. eqn

**Osservazioni:**

Le equazioni sono definite dalla valutazione di un'espressione di testo che ha il formato generale di un'operazione seguita da un massimo di tre argomenti. Ogni argomento può essere dei seguenti tipi:

-   regolazione (ad esempio, \# 2)
-   un'altra formula (ad esempio, @2 )
-   numeri fissi (ad esempio, 2)
-   valori predefiniti

La tabella seguente definisce le formule che possono essere usate con gli argomenti facoltativi in base ai nomi *v*, *P1* e *P2*. Il modello di formula è:

<f eqn=" *operation* \[*v* \] \[*p1* \] \[*p2* \]"/>



| Operazione | Parametri | Exact  | Risultato                    | Descrizione                                                                    |
|-----------|--------|--------|---------------------------|--------------------------------------------------------------------------------|
| Val       | 1      | sì    | v                         | Definisce un valore di guida da un altro valore.                                   |
| Sum       | 3      | sì    | v + P1-P2               | Utilizzato per l'addizione e la sottrazione.                                             |
| product   | 3      | giri | v \* P1/P2              | Usato per la moltiplicazione e la divisione.                                          |
| mid       | 2      | c    | (v + P1)/2               | Media.                                                                       |
| abs       | 1      | sì    | ABS (v)                    | Valore assoluto.                                                                |
| min       | 2      | sì    | min (v, P1)                 | Il valore minore di v e P1.                                                  |
| max       | 2      | sì    | Max (v, P1)                 | Il valore maggiore di v e P1.                                                 |
| if        | 3      | sì    | v > 0? P1: P2        | Test condizionale.                                                           |
| mod       | 3      | no     | sqrt (v ^ 2 + P1 ^ 2 + P2 ^ 2)   | Valore del modulo.                                                                 |
| atan2     | 2      | no     | atan2 (P1, v)               | Valore polare in gradi \* 2 ^ 16 (unità FD).                                     |
| sin       | 2      | no     | v \* sin (P1)              | Sin, argomento in gradi \* 2 ^ 16 ( [unità](msdn-online-vml-units.md) FD).     |
| cos       | 2      | no     | v \* cos (P1)              | Cos, argomento in gradi \* 2 ^ 16 ( [unità](msdn-online-vml-units.md) FD).     |
| cosatan2  | 3      | no     | v \* cos (atan2 (P2, P1))    | Conserva la precisione completa nel calcolo intermedio.                           |
| sinatan2  | 3      | no     | v \* sin (atan2 (P2, P1))    | Conserva la precisione completa nel calcolo intermedio.                           |
| sqrt      | 1      | no     | sqrt (v)                   | Il risultato è positivo e viene arrotondato per difetto.                                            |
| sumangle  | 3      | sì    | v + P1 \* 2 ^ 16 + P2 \* 2 ^ 16 | v ridimensionato di 2 ^ 16; P1 e P2 sono gradi.<br/>                            |
| ellipse   | 3      | no     | \*Sqrt di P2 (1-(v/P1) ^ 2)    | Ellisse.                                                                       |
| tan       | 2      | no     | v \* Tan (P1)              | Tangente, argomento in gradi \* 2 ^ 16 ( [unità](msdn-online-vml-units.md) FD). |



 

Si noti che l'equazione è costituita solo da operazioni e numeri; i simboli matematici vengono omessi. Ad esempio, l'equazione

EQN = "sum 5 9 3"

produrrebbe l'equivalente di

5 + 9-3

per il valore restituito di 11. Se gli operandi risultano mancanti, il valore non viene utilizzato. Ad esempio,

EQN = "sum 5 9"

produrrebbe l'equivalente di

5 + 9

e ignoreranno l'operando mancante.

*Attributo standard la*

**Esempio**

La formula seguente restituisce un risultato pari a 6 (la somma di entrambi i numeri divisi per 2), che, se si tratta della prima formula, potrebbe essere recuperata dal simbolo " @0 ".


```HTML
    <v:f eqn="mid 5 7"/>
```



 

