---
description: Contiene i dettagli relativi a una singola pagina in una nota journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5062838476e6f67605101157640a490645e454b62d852b69f51dc4bb2215db99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442801"
---
# <a name="journalpage-element"></a>Elemento JournalPage

Contiene i dettagli relativi a una singola pagina in una nota journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Stazionaria**](stationery-element.md)

[**Immagine doc**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**Contenuto**](content-element--journal-reader.md)

## <a name="attributes"></a>Attributi



| Attributo      | Type                      | Obbligatoria | Descrizione                                                                        | Valori possibili                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Necessario | Numero ordinale della pagina all'interno del documento Journal, a partire da uno (1). | Qualsiasi numero intero non negativo.                                |
| **Larghezza**      | **xs:nonNegativeInteger** | Necessario | Larghezza della pagina.                                                             | Qualsiasi numero intero non negativo.                                |
| **Altezza**     | **xs:nonNegativeInteger** | Necessario | Altezza della pagina.                                                            | Qualsiasi numero intero non negativo.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Facoltativo | Altezza della riga utilizzata nella pagina.                                           | Qualsiasi numero intero non negativo.                                |
| **Languageid** | **xs:nonNegativeInteger** | Facoltativo | ID lingua usato per la pagina.                                                 | Intero non negativo che rappresenta un ID lingua valido. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|---------------------------------------------------------------------|
| Tipo di elemento | [**complexType JournalPageType**](journalpagetype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                          |
| Nome schema  | Lettore journal                                                      |



 

 

 



