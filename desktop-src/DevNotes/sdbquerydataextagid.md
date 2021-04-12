---
description: Recupera i dati dalle voci specificate appartenenti a una voce EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401368"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="a7c3c-103">SdbQueryDataExTagID (funzione)</span><span class="sxs-lookup"><span data-stu-id="a7c3c-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="a7c3c-104">Recupera i dati dalle voci specificate appartenenti a una voce EXE.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c3c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7c3c-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="a7c3c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7c3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7c3c-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="a7c3c-109">*tiExe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-110">[**TagId**](tagid.md) della voce exe.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="a7c3c-111">*lpszDataName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-112">Nome della voce di dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="a7c3c-113">Per specificare più voci, separare i nomi con il carattere barra rovesciata (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="a7c3c-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="a7c3c-114">Se questo parametro è **null**, la funzione tenta di restituire tutte le voci di dati.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="a7c3c-115">*lpdwDataType* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-116">Tipo di dati delle voci restituite.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-116">The data type of the returned entries.</span></span> <span data-ttu-id="a7c3c-117">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7c3c-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="a7c3c-118">**REG \_ binario**</span><span class="sxs-lookup"><span data-stu-id="a7c3c-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="a7c3c-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a7c3c-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="a7c3c-120">**REG \_ - \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a7c3c-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="a7c3c-121">**REG \_ None**</span><span class="sxs-lookup"><span data-stu-id="a7c3c-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="a7c3c-122">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="a7c3c-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="a7c3c-123">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="a7c3c-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="a7c3c-124">*lpBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-125">Buffer che riceve i dati.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-125">The buffer that receives the data.</span></span> <span data-ttu-id="a7c3c-126">Se il buffer non è sufficientemente grande da contenere i dati, la funzione ha esito negativo e restituisce l' **errore \_ \_ buffer insufficiente**.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="a7c3c-127">*lpcbBufferSize* \[ in, out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-128">Dimensioni in byte del buffer *lpBuffer* .</span><span class="sxs-lookup"><span data-stu-id="a7c3c-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7c3c-129">*ptiData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c3c-130">[**TagId**](tagid.md) della voce di dati.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7c3c-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7c3c-131">Return value</span></span>

<span data-ttu-id="a7c3c-132">Questa funzione restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="a7c3c-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a7c3c-133">Return code</span></span>                                                                                                    | <span data-ttu-id="a7c3c-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7c3c-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7c3c-135"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="a7c3c-136">Uno o più parametri di input non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="a7c3c-137"><dt>**ERRORE \_ di \_ danneggiamento interno del database \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="a7c3c-138">Non sono state trovate voci di dati per la voce EXE.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="a7c3c-139"><dt>**ERRORE \_ buffer insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="a7c3c-140">Il buffer non è sufficientemente grande da contenere le voci di dati.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="a7c3c-141"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="a7c3c-142">Allocazione di memoria non riuscita.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="a7c3c-143"><dt>**ERRORE \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="a7c3c-144">Impossibile trovare una voce di dati con il nome *lpszDataName* .</span><span class="sxs-lookup"><span data-stu-id="a7c3c-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="a7c3c-145"><dt>**ERRORE \_ riuscito**</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="a7c3c-146">La funzione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="a7c3c-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="a7c3c-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7c3c-147">Requirements</span></span>



| <span data-ttu-id="a7c3c-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c3c-148">Requirement</span></span> | <span data-ttu-id="a7c3c-149">Valore</span><span class="sxs-lookup"><span data-stu-id="a7c3c-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c3c-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7c3c-150">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c3c-151">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a7c3c-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7c3c-152">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c3c-153">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7c3c-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a7c3c-154">DLL</span><span class="sxs-lookup"><span data-stu-id="a7c3c-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7c3c-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7c3c-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




