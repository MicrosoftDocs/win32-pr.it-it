---
description: Fornisce informazioni (x, y) per i punti iniziale e finale della linea di base di un paragrafo nel documento Journal. Lo spazio delle coordinate usato per questi valori è HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento Baseline
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bc64f332608b4bd0281ae2a7f29db96101e9d2e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436566"
---
# <a name="baseline-element"></a>Elemento Baseline

Fornisce informazioni (x, y) per i punti iniziale e finale della linea di base di un paragrafo nel documento Journal. Lo spazio delle coordinate usato per questi valori è **HIMETRIC.**

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Elementi padre

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuno.

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                      | Valori possibili           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Startx** | **xs:nonNegativeInteger** | Obbligatoria | Valore X per il punto che contrassegna l'inizio della linea di base. | Qualsiasi numero intero non negativo. |
| **StartY** | **xs:nonNegativeInteger** | Obbligatoria | Valore Y per il punto che contrassegna l'inizio della linea di base. | Qualsiasi numero intero non negativo. |
| **EndX**   | **xs:nonNegativeInteger** | Obbligatoria | Valore X per il punto che contrassegna la fine della linea di base.       | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|                  | Valore                                                         |
|------------------|---------------------------------------------------------------|
| **Tipo di elemento** | [**complexType BaselineType**](baselinetype-complex-type.md) |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink                    |
| **Nome schema**  | Lettore journal                                                |



 

 

 



