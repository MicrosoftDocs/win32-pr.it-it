---
description: Contiene informazioni su una parola input penna specificata nella nota Journal, incluse la posizione, le alternative e i dati effettivi sull'input penna.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313459"
---
# <a name="inkword-element"></a>Elemento InkWord

Contiene informazioni su una parola input penna specificata nella nota Journal, incluse la posizione, le alternative e i dati effettivi sull'input penna.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Elementi padre

[**Nodo del gruppo**](groupnode-element.md)

[**Linea**](line-element.md)

## <a name="child-elements"></a>Elementi figlio

[**ScalarTransform**](scalartransform-element.md)

[**Alternativa**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Attendibilità**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di delimitazione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di delimitazione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

> [!WARNING]
> Il mapping delle coordinate interne di Word Ink è costituito da unità metriche inglesi e un moltiplicatore di 2,54 deve essere usato dall'applicazione per convertire i valori di larghezza e altezza nelle unità HIMETRIC usate dalle API della piattaforma Tablet PC.

 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Tipo di elemento | ComplexType [**InkWordType**](inkwordtype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                  |
| Nome schema  | Lettore Journal                                              |



 

 

 



