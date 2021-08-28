---
description: Contiene dati binari codificati per un'immagine nel documento Journal, se presenti.
ms.assetid: fbb86bef-68f7-4aad-8a98-1c68e79ea2de
title: Elemento immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55b1cfd62dd6c2f58c2c1da26f0a9564b8c070f5c57fdccc870fa8b52b3f37c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939836"
---
# <a name="image-element"></a>Elemento immagine

Contiene dati binari codificati per un'immagine nel documento Journal, se presenti.

## <a name="definition"></a>Definizione

``` syntax
 Copy Code<xs:element name="Image" type="ImageType" />
```

## <a name="parent-elements"></a>Elementi padre

[**Contenuto**](content-element--journal-reader.md)

[**GroupNode**](groupnode-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuno.

## <a name="attributes"></a>Attributi



| Attributo  | Type                      | Obbligatoria | Descrizione                                                                             | Valori possibili           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Sinistra**   | **xs:integer**            | Necessario | Distanza tra l'origine e il punto più a sinistra nel rettangolo di selezione dell'elemento. | Qualsiasi numero intero.              |
| **Top**    | **xs:integer**            | Necessario | Distanza tra l'origine e il punto in alto nel rettangolo di selezione per l'elemento.  | Qualsiasi numero intero.              |
| **Larghezza**  | **xs:nonNegativeInteger** | Necessario | Larghezza del rettangolo di selezione per l'elemento.                                          | Qualsiasi numero intero non negativo. |
| **Altezza** | **xs:nonNegativeInteger** | Necessario | Altezza del rettangolo di selezione per l'elemento.                                         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|---------------------------------------------------------|
| Tipo di elemento | [**complexType ImageType**](imagetype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink              |
| Nome schema  | Lettore journal                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sfondo**](background-element.md)
</dt> </dl>

 

 



