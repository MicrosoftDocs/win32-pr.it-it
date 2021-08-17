---
description: Contiene informazioni su una determinata parola di input penna nella nota Journal, tra cui posizione, alternative e i dati effettivi dell'input penna.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342da6688088d37065af7af8600ac2e1e7003599914b320b21e49d39235dc712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717320"
---
# <a name="inkword-element"></a>Elemento InkWord

Contiene informazioni su una determinata parola di input penna nella nota Journal, tra cui posizione, alternative e i dati effettivi dell'input penna.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Elementi padre

[**GroupNode**](groupnode-element.md)

[**A linee**](line-element.md)

## <a name="child-elements"></a>Elementi figlio

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Attendibilità**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

> [!WARNING]
> Il mapping delle coordinate interne della parola input penna è unità metriche inglese e un moltiplicatore di 2,54 dovrà essere usato dall'applicazione per convertire i valori Width e Height nelle unità HIMETRIC usate dalle API della piattaforma Tablet PC.

 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-------------------------------------------------------------|
| Tipo di elemento | [**ComplexType InkWordType**](inkwordtype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nome schema  | Lettore journal                                              |



 

 

 



