---
title: Sezione
description: La sezione è la terza parte del flusso del set di proprietà e contiene i valori effettivi del set di proprietà.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f51891d14a9690e295379b7bcf619fe0fbe19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298127"
---
# <a name="section"></a>Sezione

La sezione è la terza parte del flusso del set di proprietà e contiene i valori effettivi del set di proprietà.

Una sezione contiene:

-   Conteggio dei byte per la sezione che include il numero di byte stesso.
-   Matrice di coppie ID/offset di proprietà a 32 bit.
-   Matrice di coppie di indicatori di tipo di proprietà/valore.

Gli offset sono la distanza dall'inizio della sezione all'inizio della coppia di proprietà (tipo, valore). Ciò consente la copia di una sezione come matrice di byte senza alcuna conversione della struttura interna.

Le pseudo strutture seguenti illustrano il formato di una sezione.

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

 

 




