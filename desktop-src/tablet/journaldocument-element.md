---
description: Elemento di primo livello in un file XML di nota del journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530169"
---
# <a name="journaldocument-element"></a>Elemento JournalDocument

Elemento di primo livello in un file XML di nota del journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>Elementi padre

Nessuna.

## <a name="child-elements"></a>Elementi figlio

[**Cancelleria**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>Attributi



| Attributo             | Type                      | Obbligatoria | Descrizione                                                      | Valori possibili           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Versione**           | **xs:string**             | Necessario | Versione del documento Journal rappresentata nel file XML. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Necessario | Larghezza predefinita della pagina per il documento Journal.          | Qualsiasi numero intero non negativo. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Necessario | Altezza predefinita della pagina per il documento Journal.         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                            |
|--------------|--------------------------------------------|
| Tipo di elemento | **JournalDocument**                        |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk |
| Nome schema  | Lettore Journal                             |



 

 

 



