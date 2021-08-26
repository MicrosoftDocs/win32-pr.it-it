---
description: ICEM10 verifica che un modulo unione contenga solo le proprietà consentite nella tabella delle proprietà.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb9634ecec212954031e665fa0ebdc3c19856a9bcd02d894eb6e579455d059b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129411"
---
# <a name="icem10"></a>ICEM10

ICEM10 verifica che un modulo unione contenga solo le proprietà consentite nella [tabella delle proprietà](property-table.md). Le proprietà specifiche del prodotto seguenti non sono consentite nella tabella delle proprietà:

-   [**Proprietà ProductLanguage**](productlanguage.md)
-   [**Proprietà ProductCode**](productcode.md)
-   [**Proprietà ProductVersion**](productversion.md)
-   [**Proprietà ProductName**](productname.md)
-   [**Proprietà Manufacturer**](manufacturer.md)

## <a name="result"></a>Risultato

ICEM10 invia un errore quando un modulo unione contiene una proprietà non consentita nella [tabella delle proprietà](property-table.md).

## <a name="example"></a>Esempio

ICEM10 invia i messaggi di errore seguenti per un modulo che contiene le voci di database visualizzate.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

Nella tabella seguente viene illustrata una tabella [delle proprietà parziale.](property-table.md)



| Proprietà                                   | Valori    |
|--------------------------------------------|-----------|
| Color                                      | Red       |
| [**Produttore**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1033      |



 

La procedura seguente illustra come correggere gli errori.

**Per correggere gli errori**

1.  Rimuovere la [**proprietà ' Manufacturer**](manufacturer.md)' dalla tabella delle [proprietà](property-table.md).
2.  Rimuovere la proprietà '[**ProductLanguage**](productlanguage.md)' dalla [tabella delle proprietà](property-table.md).

## <a name="table-used-during-execution"></a>Tabella usata durante l'esecuzione

La [tabella delle proprietà viene](property-table.md) usata durante l'esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul modulo di unione ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



