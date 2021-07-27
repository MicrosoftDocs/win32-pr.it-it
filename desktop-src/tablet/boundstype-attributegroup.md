---
description: Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file XML journal. Contiene gli attributi usati per definire i limiti (sinistro, superiore, altezza e larghezza) di un elemento nel documento.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Gruppo di attributi BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c51fcb9bc0041bbc030f2c67e434a964212562
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436510"
---
# <a name="boundstype-attribute-group"></a>Gruppo di attributi BoundsType

Definisce un gruppo di attributi utilizzato da un'ampia gamma di elementi in un file XML journal. Contiene gli attributi usati per definire i limiti (sinistro, superiore, altezza e larghezza) di un elemento nel documento.

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

Nessuno.

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                                        | Valori possibili                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Sinistra**   | **xs:integer**            | Obbligatoria | Distanza dall'origine al punto più a sinistra nel rettangolo di selezione per l'elemento.<br/> | Qualsiasi numero intero.<br/>              |
| **Top**    | **xs:integer**            | Obbligatoria | Distanza tra l'origine e il punto più in alto nel rettangolo di selezione per l'elemento.<br/>  | Qualsiasi numero intero.<br/>              |
| **Larghezza**  | **xs:nonNegativeInteger** | Obbligatoria | Larghezza del rettangolo di selezione per l'elemento.<br/>                                          | Qualsiasi numero intero non negativo.<br/> |
| **Altezza** | **xs:nonNegativeInteger** | Obbligatoria | Altezza del rettangolo di selezione per l'elemento.<br/>                                         | Qualsiasi numero intero non negativo.<br/> |



 

## <a name="type-information"></a>Informazioni sul tipo



|                 | Valore                                      |
|-----------------|--------------------------------------------|
| **Namespace**   | urn:schemas-microsoft-com:tabletpc:richink |
| **Nome schema** | Lettore journal                             |



 

## <a name="remarks"></a>Commenti

**Left** e **Top** possono essere negativi perché l'origine è definita dai margini, non dalla pagina.

 

 




