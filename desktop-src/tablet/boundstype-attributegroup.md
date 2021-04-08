---
description: Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file journal XML. Contiene gli attributi utilizzati per definire i limiti (Left, top, Height e Width) di un elemento del documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Gruppo di attributi BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749106"
---
# <a name="boundstype-attribute-group"></a>Gruppo di attributi BoundsType

Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file journal XML. Contiene gli attributi utilizzati per definire i limiti (Left, top, Height e Width) di un elemento del documento.

## <a name="definition"></a>Definizione

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a>Elementi figlio

Nessuna.

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



 

## <a name="remarks"></a>Commenti

**Left** e **Top** possono essere negativi perché l'origine è definita dai margini e non dalla pagina.

 

 




