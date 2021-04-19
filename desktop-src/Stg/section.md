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
# <a name="section"></a><span data-ttu-id="9afb2-103">Sezione</span><span class="sxs-lookup"><span data-stu-id="9afb2-103">Section</span></span>

<span data-ttu-id="9afb2-104">La sezione è la terza parte del flusso del set di proprietà e contiene i valori effettivi del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="9afb2-104">The section is the third part of the property set stream and contains the actual property set values.</span></span>

<span data-ttu-id="9afb2-105">Una sezione contiene:</span><span class="sxs-lookup"><span data-stu-id="9afb2-105">A section contains:</span></span>

-   <span data-ttu-id="9afb2-106">Conteggio dei byte per la sezione che include il numero di byte stesso.</span><span class="sxs-lookup"><span data-stu-id="9afb2-106">Byte count for the section which is inclusive of the byte count itself.</span></span>
-   <span data-ttu-id="9afb2-107">Matrice di coppie ID/offset di proprietà a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="9afb2-107">Array of 32-bit Property ID/Offset pairs.</span></span>
-   <span data-ttu-id="9afb2-108">Matrice di coppie di indicatori di tipo di proprietà/valore.</span><span class="sxs-lookup"><span data-stu-id="9afb2-108">Array of property Type Indicators/Value pairs.</span></span>

<span data-ttu-id="9afb2-109">Gli offset sono la distanza dall'inizio della sezione all'inizio della coppia di proprietà (tipo, valore).</span><span class="sxs-lookup"><span data-stu-id="9afb2-109">Offsets are the distance from the start of the section to the start of the property (type, value) pair.</span></span> <span data-ttu-id="9afb2-110">Ciò consente la copia di una sezione come matrice di byte senza alcuna conversione della struttura interna.</span><span class="sxs-lookup"><span data-stu-id="9afb2-110">This allows a section to be copied as an array of bytes without any translation of internal structure.</span></span>

<span data-ttu-id="9afb2-111">Le pseudo strutture seguenti illustrano il formato di una sezione.</span><span class="sxs-lookup"><span data-stu-id="9afb2-111">The following pseudo-structures illustrate the format of a section.</span></span>

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

 

 




