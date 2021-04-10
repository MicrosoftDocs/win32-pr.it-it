---
description: La struttura del SET definisce un set di valori.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: IMPOSTA struttura (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231533"
---
# <a name="set-structure"></a><span data-ttu-id="cb28f-103">IMPOSTA struttura</span><span class="sxs-lookup"><span data-stu-id="cb28f-103">SET structure</span></span>

<span data-ttu-id="cb28f-104">La struttura del **set** definisce un set di valori.</span><span class="sxs-lookup"><span data-stu-id="cb28f-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb28f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb28f-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="cb28f-106">Members</span><span class="sxs-lookup"><span data-stu-id="cb28f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb28f-107">**nEntries**</span><span class="sxs-lookup"><span data-stu-id="cb28f-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-108">Numero totale di voci in un set.</span><span class="sxs-lookup"><span data-stu-id="cb28f-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-109">**lpByteTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-110">Puntatore a una matrice di valori di BYTE.</span><span class="sxs-lookup"><span data-stu-id="cb28f-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-111">**lpWordTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-112">Puntatore a una matrice di valori di WORD.</span><span class="sxs-lookup"><span data-stu-id="cb28f-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-113">**lpDwordTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-114">Puntatore a una matrice di valori DWORD.</span><span class="sxs-lookup"><span data-stu-id="cb28f-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-115">**lpLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-116">Puntatore a una matrice di strutture [largeInt](largeint.md) .</span><span class="sxs-lookup"><span data-stu-id="cb28f-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-117">**lpSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-118">Puntatore a una matrice di valori SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="cb28f-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-119">**lpLabeledByteTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-120">Puntatore a una matrice di strutture di [ \_ byte con etichetta](labeled-byte.md) .</span><span class="sxs-lookup"><span data-stu-id="cb28f-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="cb28f-121">Ogni struttura di **\_ byte con etichetta** definisce un valore e un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="cb28f-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="cb28f-122">Network Monitor visualizza un'etichetta se trova un valore corrispondente nel pacchetto del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb28f-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-123">**lpLabeledWordTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-124">Puntatore a una matrice di strutture di [ \_ Word con etichetta](labeled-word.md) che definiscono un set di valori di Word ed etichette.</span><span class="sxs-lookup"><span data-stu-id="cb28f-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-125">**lpLabeledDwordTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-126">Puntatore a una matrice di strutture [ \_ DWORD con etichetta](labeled-dword.md) che definiscono un set di valori DWORD ed etichette.</span><span class="sxs-lookup"><span data-stu-id="cb28f-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-127">**lpLabeledLargeIntTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-128">Puntatore a una matrice di strutture [ \_ largeInt con etichetta](labeled-largeint.md) che definiscono un set di valori largeInt ed etichette.</span><span class="sxs-lookup"><span data-stu-id="cb28f-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-129">**lpLabeledSystemTimeTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-130">Puntatore a una matrice di strutture [ \_ SYSTEMTIME con etichetta](labeled-systemtime.md) che definiscono un set di valori di sistema ed etichette.</span><span class="sxs-lookup"><span data-stu-id="cb28f-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-131">**lpLabeledBit**</span><span class="sxs-lookup"><span data-stu-id="cb28f-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-132">Puntatore a una matrice di strutture di [ \_ bit con etichetta](labeled-bit.md) che definiscono un set di coppie di bit con etichetta.</span><span class="sxs-lookup"><span data-stu-id="cb28f-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="cb28f-133">Ogni BIT può specificare due etichette un'etichetta per ogni stato (0 o 1) del BIT.</span><span class="sxs-lookup"><span data-stu-id="cb28f-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="cb28f-134">**lpVoidTable**</span><span class="sxs-lookup"><span data-stu-id="cb28f-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="cb28f-135">Puntatore a una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="cb28f-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb28f-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb28f-136">Remarks</span></span>

<span data-ttu-id="cb28f-137">La struttura del **set** viene utilizzata per definire un set di dati di confronto che Network Monitor possibile utilizzare per interpretare il valore di una proprietà in un pacchetto di protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb28f-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="cb28f-138">Quando è necessario un set di dati di confronto, nel membro **lpSet** della struttura [PROPERTYINFO](propertyinfo.md) viene specificato un puntatore alla struttura del **set** .</span><span class="sxs-lookup"><span data-stu-id="cb28f-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="cb28f-139">La DLL del parser può fornire un set di valori e un set di etichette.</span><span class="sxs-lookup"><span data-stu-id="cb28f-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="cb28f-140">Il membro dell' **Unione** selezionato in una struttura **set** punta a una matrice di strutture che definiscono ogni membro di un set.</span><span class="sxs-lookup"><span data-stu-id="cb28f-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="cb28f-141">Valore impostato</span><span class="sxs-lookup"><span data-stu-id="cb28f-141">Value set</span></span>

    <span data-ttu-id="cb28f-142">Un set di valori viene utilizzato quando si desidera che Network Monitor includa un indicatore set o not-in set con il valore trovato nel pacchetto del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cb28f-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="cb28f-143">Se, ad esempio, viene specificato un set DWORD, Network Monitor visualizza un'etichetta per ogni valore DWORD trovato nel pacchetto di protocollo, che indica che il valore DWORD è o non è specificato nel set.</span><span class="sxs-lookup"><span data-stu-id="cb28f-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="cb28f-144">Un set di valori può essere basato sui tipi di dati BYTE, WORD, DWORD, LARGEINT e SYSTEMTIME.</span><span class="sxs-lookup"><span data-stu-id="cb28f-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="cb28f-145">Set di etichette</span><span class="sxs-lookup"><span data-stu-id="cb28f-145">Label set</span></span>

    <span data-ttu-id="cb28f-146">Viene utilizzato un set di etichette quando si desidera che Network Monitor visualizzi un'etichetta definita dall'utente anziché i valori di proprietà specificati in un set.</span><span class="sxs-lookup"><span data-stu-id="cb28f-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="cb28f-147">Un set di etichette può essere basato sulle coppie BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME e BIT Label.</span><span class="sxs-lookup"><span data-stu-id="cb28f-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb28f-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb28f-148">Requirements</span></span>



| <span data-ttu-id="cb28f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb28f-149">Requirement</span></span> | <span data-ttu-id="cb28f-150">Valore</span><span class="sxs-lookup"><span data-stu-id="cb28f-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cb28f-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb28f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="cb28f-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb28f-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cb28f-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb28f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="cb28f-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cb28f-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cb28f-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb28f-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb28f-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb28f-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb28f-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb28f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb28f-158">con etichetta \_ bit</span><span class="sxs-lookup"><span data-stu-id="cb28f-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="cb28f-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="cb28f-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




