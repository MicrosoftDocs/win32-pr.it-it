---
description: Contiene informazioni di testo dalla nota Journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Elemento Text
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae4e9fa123f1f43bd92d902158fc3fbc5b1c1de8e074b57aadeb339a0a7b6f15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819940"
---
# <a name="text-element"></a>Elemento Text

Contiene informazioni di testo dalla nota Journal.

## <a name="definition"></a>Definizione

Se usato con [**Content:**](content-element--journal-reader.md)

``` syntax
<xs:element name="Text" type="TextType" />
```

Oppure, se usato con [**TitleInfo**](titleinfo-element.md) e [**GroupNode:**](groupnode-element.md)

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

Non sono presenti attributi se usati con [**TitleInfo**](titleinfo-element.md) e [**GroupNode.**](groupnode-element.md) Se usati con [**Content,**](content-element--journal-reader.md)gli attributi sono i seguenti.



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di selezione dell'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|   Elemento           |   valore                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo di elemento | [**complexType TextType**](texttype-complex-type.md) (con l'elemento Content) **o xs:string** (con [**elementi GroupNode**](groupnode-element.md) [**e TitleInfo)**](titleinfo-element.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink<br/>                                                                                                                                               |
| Nome schema  | Lettore journal<br/>                                                                                                                                                                           |



 

 

 




