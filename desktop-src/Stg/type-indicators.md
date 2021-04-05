---
title: Indicatori di tipo
description: Le proprietà effettive seguono la tabella dei valori del set di proprietà coppie di identificatori di proprietà/offset. Ogni proprietà viene archiviata come DWORD, seguita dal valore del tipo di dati.
ms.assetid: 8523458b-8b1b-4e9f-8f96-d7601e57675c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8383a860f07e908b72a7b25091f3cc2e280e4407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047105"
---
# <a name="type-indicators"></a><span data-ttu-id="3e5d5-104">Indicatori di tipo</span><span class="sxs-lookup"><span data-stu-id="3e5d5-104">Type Indicators</span></span>

<span data-ttu-id="3e5d5-105">Le proprietà effettive seguono la tabella dei valori del set di proprietà coppie di identificatori di proprietà/offset.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-105">The actual properties follow the table of Property Identifiers/Offset Pairs property set values.</span></span> <span data-ttu-id="3e5d5-106">Ogni proprietà viene archiviata come **DWORD**, seguita dal valore del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-106">Each property is stored as a **DWORD**, followed by the data type value.</span></span>

<span data-ttu-id="3e5d5-107">Gli indicatori di tipo e i relativi valori associati sono descritti nella struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="3e5d5-107">Type indicators and their associated values are described in the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="3e5d5-108">Tutte le coppie tipo/valore devono iniziare con un limite di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-108">All Type/Value pairs must begin on a 32-bit boundary.</span></span> <span data-ttu-id="3e5d5-109">Pertanto, i valori possono essere seguiti con byte null per allineare la coppia successiva in un limite di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-109">Thus, values may be followed with null bytes to align the subsequent pair on a 32-bit boundary.</span></span>

<span data-ttu-id="3e5d5-110">Il codice di esempio seguente calcola il numero di byte necessari per l'allineamento su un limite a 32 bit, dato un conteggio di byte.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-110">The following example code calculates how many bytes are required to align on a 32-bit boundary, given a count of bytes.</span></span>


```C++
cbAdd = (((cbCurrent + 3) >> 2) << 2) - cbCurrent ;
```



<span data-ttu-id="3e5d5-111">All'interno di un vettore di valori, ogni ripetizione di un valore scalare semplice inferiore a 32 bit deve essere allineata con il relativo allineamento naturale anziché con un allineamento a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-111">Within a vector of values, each repetition of a simple scalar value smaller than 32 bits must align with its natural alignment rather than with a 32-bit alignment.</span></span> <span data-ttu-id="3e5d5-112">In pratica, questa operazione è significativa solo per i tipi **VT \_ Ui1**, **VT \_ UI2**, **VT \_ I2** e **VT \_ bool** (che hanno un allineamento naturale a un byte o a due byte).</span><span class="sxs-lookup"><span data-stu-id="3e5d5-112">In practice, this is only significant for types **VT\_UI1**, **VT\_UI2**, **VT\_I2**, and **VT\_BOOL** (which have one-byte or two-byte natural alignment).</span></span> <span data-ttu-id="3e5d5-113">Tutti gli altri tipi hanno un allineamento naturale a quattro byte.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-113">All other types have four-byte natural alignment.</span></span> <span data-ttu-id="3e5d5-114">Alcuni tipi, ad esempio, **VT \_ R8**, hanno effettivamente un allineamento naturale a 8 byte, ma vengono archiviati come se avessero un allineamento a quattro byte.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-114">Some types, for example, **VT\_R8**, actually have 8-byte natural alignment, but are stored as if they have four-byte alignment.</span></span>

<span data-ttu-id="3e5d5-115">Un valore della proprietà con l'indicatore di tipo **VT \_ I2** \| **VT \_ vector** include:</span><span class="sxs-lookup"><span data-stu-id="3e5d5-115">A property value with type indicator **VT\_I2** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="3e5d5-116">Conteggio di elementi **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3e5d5-116">A **DWORD** element count.</span></span>
-   <span data-ttu-id="3e5d5-117">Sequenza di interi a due byte compressi senza spaziatura interna null.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-117">A sequence of packed two-byte integers with no null padding between them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e5d5-118">Tutti i conteggi a 32 bit o i tipi di proprietà archiviati come parte di un elemento della proprietà Vector devono anche essere allineati a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-118">Any 32-bit counts or property types that are stored as a part of a vector property element must also be 32-bit aligned.</span></span>

 

<span data-ttu-id="3e5d5-119">Il valore della proprietà dell'identificatore di tipo **VT \_ LPSTR** \| **VT \_ vector** include:</span><span class="sxs-lookup"><span data-stu-id="3e5d5-119">A property value of type identifier **VT\_LPSTR** \| **VT\_VECTOR** would include:</span></span>

-   <span data-ttu-id="3e5d5-120">Un conteggio di elementi **DWORD** (**DWORD** *cElems*).</span><span class="sxs-lookup"><span data-stu-id="3e5d5-120">A **DWORD** element count (**DWORD** *cElems*).</span></span>
-   <span data-ttu-id="3e5d5-121">Sequenza di stringhe (**char** *rgch \[ \]*), ognuna preceduta da un **valore DWORD** di lunghezza e possibilmente seguito da una spaziatura interna null per arrotondare a un limite di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3e5d5-121">A sequence of strings (**char** *rgch\[\]*), each preceded by a length-count **DWORD** and possibly followed by null padding to round to a 32-bit boundary.</span></span>

 

 