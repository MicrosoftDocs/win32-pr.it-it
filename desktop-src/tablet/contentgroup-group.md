---
description: Definisce un gruppo che contiene un set di contenuto raggruppato in una nota journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Gruppo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432613"
---
# <a name="contentgroup-group"></a>Gruppo ContentGroup

Definisce un gruppo che contiene un set di contenuto raggruppato in una nota journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementi figlio

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Inkword**](inkword-element.md)

[**Disegno**](drawing-element.md)

[**Text**](text-element.md)

[**Immagine**](docimage-element.md)

[**Bandiera**](flag-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                                        | Valori possibili                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Sinistra**   | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.<br/> | Qualsiasi numero intero.<br/>              |
| **Top**    | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più in alto nel rettangolo di selezione per l'elemento.<br/>  | Qualsiasi numero intero.<br/>              |
| **Larghezza**  | **xs:nonNegativeInteger** | Obbligatoria | Larghezza del rettangolo di selezione per l'elemento.<br/>                                          | Qualsiasi numero intero non negativo.<br/> |
| **Altezza** | **xs:nonNegativeInteger** | Obbligatoria | Altezza del rettangolo di selezione per l'elemento.<br/>                                         | Qualsiasi numero intero non negativo.<br/> |



 

## <a name="type-information"></a>Informazioni sul tipo



|  Elemento     | valore                                                     |
|-------------|--------------------------------------------|
| Spazio dei nomi   | urn:schemas-microsoft-com:tabletpc:richink |
| Nome schema | Lettore journal                             |



 

 

 




