---
description: Contiene i dati binari codificati per un'immagine nel documento Journal, se presente.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8437495a4c248a8e5bc68a0f7b75a2cf7d761387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314926"
---
# <a name="image-element"></a>Elemento immagine

Contiene i dati binari codificati per un'immagine nel documento Journal, se presente.

## <a name="definition"></a>Definizione

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**Nodo del gruppo**](groupnode-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuna.

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di delimitazione per l'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto superiore del rettangolo di delimitazione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di delimitazione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di delimitazione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                         |
|--------------|---------------------------------------------------------|
| Tipo di elemento | ComplexType [**ImageType**](imagetype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk              |
| Nome schema  | Lettore Journal                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sfondo**](background-element.md)
</dt> </dl>

 

 



