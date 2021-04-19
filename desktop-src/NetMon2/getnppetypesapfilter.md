---
description: La funzione GetNPPEtypeSapFilter Recupera il filtro ETYPE/SAP da un BLOB specificato.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: Funzione GetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319947"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="3ddcc-103">GetNPPEtypeSapFilter (funzione)</span><span class="sxs-lookup"><span data-stu-id="3ddcc-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="3ddcc-104">La funzione **GetNPPEtypeSapFilter** Recupera il filtro ETYPE/SAP da un blob specificato.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ddcc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ddcc-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="3ddcc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ddcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ddcc-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-109">*pnSaps* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-110">Puntatore al numero di protocolli restituito nella tabella SAP.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-111">*pnEtypes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-112">Puntatore al numero restituito di ETYPE del nella tabella etype.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-113">*ppSapTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-114">Puntatore alla tabella SAP restituita.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-115">*ppEtypeTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-116">Puntatore alla tabella ETYPE restituita.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-117">*pFilterFlags* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-118">Puntatore ai flag di filtro restituiti.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="3ddcc-119">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ddcc-120">Handle per un BLOB di errore, che specifica la posizione nel BLOB originale in cui si è verificato l'errore (se presente).</span><span class="sxs-lookup"><span data-stu-id="3ddcc-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ddcc-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ddcc-121">Return value</span></span>

<span data-ttu-id="3ddcc-122">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3ddcc-123">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ddcc-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ddcc-124">Remarks</span></span>

<span data-ttu-id="3ddcc-125">Le informazioni su ETYPE/SAP sono archiviate nella categoria **config** della sezione del **proprietario** di NPP.</span><span class="sxs-lookup"><span data-stu-id="3ddcc-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ddcc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ddcc-126">Requirements</span></span>



| <span data-ttu-id="3ddcc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ddcc-127">Requirement</span></span> | <span data-ttu-id="3ddcc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3ddcc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ddcc-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ddcc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3ddcc-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3ddcc-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ddcc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3ddcc-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ddcc-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ddcc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ddcc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ddcc-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ddcc-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3ddcc-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ddcc-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ddcc-136"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ddcc-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3ddcc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3ddcc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ddcc-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ddcc-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ddcc-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ddcc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ddcc-140">SetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="3ddcc-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




