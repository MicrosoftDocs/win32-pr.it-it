---
description: Contiene i dettagli relativi a una singola pagina in una nota del journal.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Elemento JournalPage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883418"
---
# <a name="journalpage-element"></a>Elemento JournalPage

Contiene i dettagli relativi a una singola pagina in una nota del journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Stazionaria**](stationery-element.md)

[**DocImage**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**Contenuto**](content-element--journal-reader.md)

## <a name="attributes"></a>Attributi



| Attributo      | Type                      | Obbligatoria | Descrizione                                                                        | Valori possibili                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Necessario | Numero ordinale della pagina all'interno del documento Journal, a partire da uno (1). | Qualsiasi numero intero non negativo.                                |
| **Larghezza**      | **xs:nonNegativeInteger** | Necessario | Larghezza della pagina.                                                             | Qualsiasi numero intero non negativo.                                |
| **Altezza**     | **xs:nonNegativeInteger** | Necessario | Altezza della pagina.                                                            | Qualsiasi numero intero non negativo.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Facoltativo | Altezza della riga utilizzata nella pagina.                                           | Qualsiasi numero intero non negativo.                                |
| **LanguageId** | **xs:nonNegativeInteger** | Facoltativo | ID lingua utilizzato per la pagina.                                                 | Intero non negativo che rappresenta un ID lingua valido. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| Tipo di elemento | ComplexType [**JournalPageType**](journalpagetype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                          |
| Nome schema  | Lettore Journal                                                      |



 

 

 



