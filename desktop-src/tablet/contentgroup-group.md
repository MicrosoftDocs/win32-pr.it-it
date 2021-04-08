---
description: Definisce un gruppo che contiene un set di contenuto raggruppato in una nota del journal.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Gruppo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbbc13a3dee796646b6d61ac9ba0bde50880f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057894"
---
# <a name="contentgroup-group"></a>Gruppo ContentGroup

Definisce un gruppo che contiene un set di contenuto raggruppato in una nota del journal.

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

[**Nodo del gruppo**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Disegno**](drawing-element.md)

[**Text**](text-element.md)

[**Immagine**](docimage-element.md)

[**Contrassegno**](flag-element.md)

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento.<br/> | Qualsiasi numero intero.<br/>              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.<br/>  | Qualsiasi numero intero.<br/>              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di delimitazione per l'elemento.<br/>                                          | Qualsiasi numero intero non negativo.<br/> |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di delimitazione per l'elemento.<br/>                                         | Qualsiasi numero intero non negativo.<br/> |



 

## <a name="type-information"></a>Informazioni sul tipo



|             |                                            |
|-------------|--------------------------------------------|
| Spazio dei nomi   | urn: schemas-microsoft-com: TabletPC: RichInk |
| Nome schema | Lettore Journal                             |



 

 

 




