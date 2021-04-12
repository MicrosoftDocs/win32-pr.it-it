---
description: Imposta il filtro ETYPE/SAP del BLOB.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: Funzione SetNPPEtypeSapFilter (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344961"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="b264e-103">SetNPPEtypeSapFilter (funzione)</span><span class="sxs-lookup"><span data-stu-id="b264e-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="b264e-104">La funzione **SetNPPEtypeSapFilter** imposta il filtro ETYPE/SAP del BLOB.</span><span class="sxs-lookup"><span data-stu-id="b264e-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="b264e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b264e-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b264e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b264e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b264e-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b264e-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="b264e-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="b264e-109">*nSaps* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b264e-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-110">Numero di succhi.</span><span class="sxs-lookup"><span data-stu-id="b264e-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="b264e-111">*nEtypes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b264e-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-112">Numero di ETYPE del nella tabella etype da impostare.</span><span class="sxs-lookup"><span data-stu-id="b264e-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="b264e-113">*lpSapTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b264e-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-114">Puntatore alla tabella SAP impostata.</span><span class="sxs-lookup"><span data-stu-id="b264e-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="b264e-115">*lpEtypeTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b264e-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-116">Puntatore alla tabella ETYPE impostata.</span><span class="sxs-lookup"><span data-stu-id="b264e-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="b264e-117">*FilterFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b264e-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-118">Flag di filtro impostati.</span><span class="sxs-lookup"><span data-stu-id="b264e-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="b264e-119">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b264e-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b264e-120">Handle per un BLOB di errori che specifica il punto in cui si è verificato l'errore (se presente) nel BLOB originale.</span><span class="sxs-lookup"><span data-stu-id="b264e-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b264e-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b264e-121">Return value</span></span>

<span data-ttu-id="b264e-122">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="b264e-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="b264e-123">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="b264e-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b264e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b264e-124">Requirements</span></span>



| <span data-ttu-id="b264e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b264e-125">Requirement</span></span> | <span data-ttu-id="b264e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b264e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b264e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b264e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b264e-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b264e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b264e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b264e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b264e-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b264e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b264e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b264e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b264e-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b264e-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="b264e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="b264e-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b264e-134"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b264e-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="b264e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b264e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b264e-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b264e-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b264e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b264e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b264e-138">GetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="b264e-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




