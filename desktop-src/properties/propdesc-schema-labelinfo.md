---
description: Specifica la modalità di visualizzazione delle etichette della proprietà.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d2d358270bfdf231f990feee54d90f6f39f16fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475097"
---
# <a name="labelinfo"></a>labelInfo

Specifica la modalità di visualizzazione delle etichette della proprietà. Deve essere presente un solo [elemento labelInfo]() per ogni [elemento propertyDescription.](./propdesc-schema-propertydescription.md)

Se sono presenti più elementi, viene usato l'ultimo. Se non viene specificato alcun elemento [labelInfo,]() l'etichetta della proprietà non viene visualizzata; Tuttavia, in genere si tratta di un difetto.

## <a name="syntax"></a>Sintassi


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                   | Elementi figlio |
|------------------------------------------------------------------|----------------|
| [proprietàDescrizione](./propdesc-schema-propertydescription.md) | Nessuno           |



 

## <a name="attributes"></a>Attributi




| Attributo | Descrizione | 
|-----------|-------------|
| label | Pubblica. facoltativo. Etichetta visualizzata nell'interfaccia utente, ad esempio l'etichetta della colonna dei dettagli o il riquadro di anteprima. La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto alla stringa di visualizzazione. Usare la stringa di visualizzazione indiretta perché può essere localizzata. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> restituisce il nome visualizzato risolto. | 
| Sortdescription | facoltativo. Specifica le stringhe offerte come opzioni di ordinamento. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> restituisce questa descrizione dell'ordinamento. I valori seguenti forniscono le stringhe dell'interfaccia utente corrispondenti.<ul><li>Generale: "Sort going up" / "Sort going down"</li><li>AToZ: "A on top" / "Z on top"</li><li>LowestHighest: "Lowest on top" / "Highest on top"</li><li>Meno recenteNewest: "Oldest on top" / "Newest on top"</li><li>SmallestLargest: "Smallest on top" / "Largest on top"</li></ul> | 
| invitationText | facoltativo. Testo della stringa della Guida visualizzato come istruzione per l'utente per il controllo o la descrizione comando, ad esempio "Immettere il nome dell'autore". La sintassi consente una stringa di visualizzazione diretta o un riferimento indiretto alla stringa di visualizzazione. Usare la stringa di visualizzazione indiretta perché può essere localizzata. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> restituisce il testo di invito risolto. | 
| hideLabel | facoltativo. Il valore predefinito è "false". Indica se l'etichetta è nascosta. | 




 

 

 
