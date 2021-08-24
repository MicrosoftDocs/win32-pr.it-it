---
title: Sezione
description: La sezione è la terza parte del flusso del set di proprietà e contiene i valori effettivi del set di proprietà.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bca5dd2801e437ecfffe663f2702abc4c202d721ecbda8a9b95656e40a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682801"
---
# <a name="section"></a>Sezione

La sezione è la terza parte del flusso del set di proprietà e contiene i valori effettivi del set di proprietà.

Una sezione contiene:

-   Numero di byte per la sezione inclusiva del conteggio dei byte stesso.
-   Matrice di coppie ID proprietà/offset a 32 bit.
-   Matrice di coppie di indicatori di tipo/valore della proprietà.

Gli offset sono la distanza dall'inizio della sezione all'inizio della coppia di proprietà (tipo, valore). In questo modo una sezione può essere copiata come matrice di byte senza alcuna conversione della struttura interna.

Le pseudo-strutture seguenti illustrano il formato di una sezione.

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




