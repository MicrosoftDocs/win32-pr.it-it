---
description: Contiene informazioni di testo dalla nota journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432320"
---
# <a name="text-element"></a>Elemento Text

Contiene informazioni di testo dalla nota journal.

## <a name="definition"></a>Definizione

Se usato con [**Content**](content-element--journal-reader.md):

``` syntax
<xs:element name="Text" type="TextType" />
```

Oppure, se usato con [**TitleInfo**](titleinfo-element.md) e [**GroupNode**](groupnode-element.md):

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

[**TitleInfo**](titleinfo-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuno.

## <a name="attributes"></a>Attributi

Non sono presenti attributi quando vengono usati [**con TitleInfo**](titleinfo-element.md) e [**GroupNode.**](groupnode-element.md) Se usati con [**Content,**](content-element--journal-reader.md)gli attributi sono i seguenti.



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Obbligatoria | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Obbligatoria | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|   Elemento           |   valore                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento | [**ComplexType**](texttype-complex-type.md) TextType (con l'elemento Content) o **xs:string** (con [**elementi GroupNode**](groupnode-element.md) [**e TitleInfo)**](titleinfo-element.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink<br/>                                                                                                                                               |
| Nome schema  | Lettore journal<br/>                                                                                                                                                                           |



 

 

 




