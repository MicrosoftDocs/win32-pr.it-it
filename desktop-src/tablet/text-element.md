---
description: Contiene informazioni sul testo della nota Journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968416"
---
# <a name="text-element"></a>Elemento Text

Contiene informazioni sul testo della nota Journal.

## <a name="definition"></a>Definizione

Se usato con [**contenuto**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

In alternativa, se usato con [**TitleInfo**](titleinfo-element.md) e [**nodo del gruppo**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**Nodo del gruppo**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuna.

## <a name="attributes"></a>Attributi

Non sono presenti attributi se usati con [**TitleInfo**](titleinfo-element.md) e [**nodo del gruppo**](groupnode-element.md). Quando viene usato con il [**contenuto**](content-element--journal-reader.md), gli attributi sono i seguenti.



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di delimitazione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di delimitazione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento | [**Texttype**](texttype-complex-type.md) ComplexType (con l'elemento Content) o **xs: String** (con elementi [**nodo del gruppo**](groupnode-element.md) e [**TitleInfo**](titleinfo-element.md) ) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk<br/>                                                                                                                                               |
| Nome schema  | Lettore Journal<br/>                                                                                                                                                                           |



 

 

 




