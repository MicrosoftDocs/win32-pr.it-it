---
description: ICEM10 verifica che un modulo merge includa solo le proprietà consentite nella tabella delle proprietà.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314789"
---
# <a name="icem10"></a>ICEM10

ICEM10 verifica che un modulo merge includa solo le proprietà consentite nella [tabella delle proprietà](property-table.md). Nella tabella delle proprietà non sono consentite le seguenti proprietà specifiche del prodotto:

-   [**Proprietà ProductLanguage**](productlanguage.md)
-   [**Proprietà ProductCode**](productcode.md)
-   [**Proprietà ProductVersion**](productversion.md)
-   [**Proprietà ProductName**](productname.md)
-   [**Proprietà produttore**](manufacturer.md)

## <a name="result"></a>Risultato

ICEM10 Invia un errore quando un modulo merge contiene una proprietà non consentita nella [tabella delle proprietà](property-table.md).

## <a name="example"></a>Esempio

ICEM10 invia i messaggi di errore seguenti per un modulo che contiene le voci di database indicate.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

Nella tabella seguente viene illustrata una [tabella delle proprietà](property-table.md)parziali.



| Proprietà                                   | Valori    |
|--------------------------------------------|-----------|
| Colore                                      | Red       |
| [**Produttore**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 1033      |



 

Nella procedura riportata di seguito viene illustrato come correggere gli errori.

**Per correggere gli errori**

1.  Rimuovere la proprietà'[**Manufacturer**](manufacturer.md)' dalla [tabella delle proprietà](property-table.md).
2.  Rimuovere la proprietà'[**ProductLanguage**](productlanguage.md)' dalla [tabella delle proprietà](property-table.md).

## <a name="table-used-during-execution"></a>Tabella utilizzata durante l'esecuzione

La [tabella delle proprietà](property-table.md) viene utilizzata durante l'esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio del modulo merge](merge-module-ice-reference.md)
</dt> </dl>

 

 



