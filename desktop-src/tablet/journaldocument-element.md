---
description: Elemento di primo livello in un file XML di nota journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Elemento JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432173"
---
# <a name="journaldocument-element"></a>Elemento JournalDocument

Elemento di primo livello in un file XML di nota journal.

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

Nessuno.

## <a name="child-elements"></a>Elementi figlio

[**Cancelleria**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>Attributi



| Attributo             | Type                      | Obbligatoria | Descrizione                                                      | Valori possibili           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Versione**           | **xs:string**             | Obbligatoria | Versione del documento Journal rappresentata nel file XML. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Obbligatoria | Larghezza predefinita della pagina per il documento Journal.          | Qualsiasi numero intero non negativo. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Obbligatoria | Altezza predefinita della pagina per il documento Journal.         | Qualsiasi numero intero non negativo. |



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|--------------------------------------------|
| Tipo di elemento | **JournalDocument**                        |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink |
| Nome schema  | Lettore journal                             |



 

 

 



