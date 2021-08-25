---
description: Contiene una bitmap con codifica Base64 di un flag associato alla sezione di una nota journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Elemento Flag
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df40874178ba998ae9c864036b7befbf85179680de92cb68595f394e370e4404
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774081"
---
# <a name="flag-element"></a>Elemento Flag

Contiene una bitmap con codifica Base64 di un flag associato alla sezione di una nota journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
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
|--------------|-------------------------------------------------------|
| Tipo di elemento | [**complexType FlagType**](flagtype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink            |
| Nome schema  | Lettore journal                                        |



 

 

 



