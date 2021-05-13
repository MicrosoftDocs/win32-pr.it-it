---
description: Contiene informazioni che definiscono un nuovo elenco degli elementi usati più di recente. Usato da CreateMRUListW.
title: Struttura MRUINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840762"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="f1536-104">Struttura MRUINFO</span><span class="sxs-lookup"><span data-stu-id="f1536-104">MRUINFO structure</span></span>

<span data-ttu-id="f1536-105">Contiene informazioni che definiscono un nuovo elenco degli elementi usati più di recente.</span><span class="sxs-lookup"><span data-stu-id="f1536-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="f1536-106">Usato da [**CreateMRUListW.**](createmrulist.md)</span><span class="sxs-lookup"><span data-stu-id="f1536-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1536-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1536-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="f1536-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1536-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1536-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="f1536-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="f1536-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f1536-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f1536-111">Dimensione della struttura .</span><span class="sxs-lookup"><span data-stu-id="f1536-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="f1536-112">**Umax**</span><span class="sxs-lookup"><span data-stu-id="f1536-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="f1536-113">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="f1536-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="f1536-114">Numero massimo di voci nell'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="f1536-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="f1536-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="f1536-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f1536-116">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="f1536-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="f1536-117">Uno o più dei flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1536-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="f1536-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="f1536-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="f1536-119">I dati vengono archiviati nel Registro di sistema come dati binari anziché come dati stringa.</span><span class="sxs-lookup"><span data-stu-id="f1536-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="f1536-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="f1536-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="f1536-121">Scrivere le modifiche alla versione dell'elenco MRU archiviata nel Registro di sistema solo quando viene aggiunto un nuovo elemento o le risorse dell'elenco MRU vengono liberate dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="f1536-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="f1536-122">Si noti che la versione attiva dell'elenco MRU in memoria viene aggiornata immediatamente in risposta a qualsiasi modifica nel contenuto o nell'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="f1536-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f1536-123">**Hkey**</span><span class="sxs-lookup"><span data-stu-id="f1536-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="f1536-124">Tipo: **HKEY**</span><span class="sxs-lookup"><span data-stu-id="f1536-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="f1536-125">Handle per la chiave attualmente aperta o uno dei valori predefiniti seguenti in cui archiviare i dati MRU.</span><span class="sxs-lookup"><span data-stu-id="f1536-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="f1536-126">**HKEY \_ CURRENT \_ USER**</span><span class="sxs-lookup"><span data-stu-id="f1536-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="f1536-127">**HKEY \_ LOCAL \_ MACHINE**</span><span class="sxs-lookup"><span data-stu-id="f1536-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f1536-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="f1536-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="f1536-129">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="f1536-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="f1536-130">Sottochiave in cui archiviare i dati MRU.</span><span class="sxs-lookup"><span data-stu-id="f1536-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="f1536-131">**lpfnCompare**</span><span class="sxs-lookup"><span data-stu-id="f1536-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="f1536-132">Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="f1536-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f1536-133">Puntatore a una funzione di confronto dei dati facoltativa che può essere usata per determinare se un elemento è presente nell'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="f1536-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="f1536-134">Ciò è utile quando l'elenco MRU è stato creato con il flag **MRU \_ BINARY.**</span><span class="sxs-lookup"><span data-stu-id="f1536-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="f1536-135">Se questo membro è **NULL,** vengono usate le funzioni standard di confronto tra stringhe. Per i dati binari, viene usato un confronto diretto della memoria.</span><span class="sxs-lookup"><span data-stu-id="f1536-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1536-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1536-136">Remarks</span></span>

<span data-ttu-id="f1536-137">Questa struttura non è definita in un file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="f1536-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="f1536-138">È necessario definirlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="f1536-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1536-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1536-139">Requirements</span></span>



| <span data-ttu-id="f1536-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1536-140">Requirement</span></span> | <span data-ttu-id="f1536-141">Valore</span><span class="sxs-lookup"><span data-stu-id="f1536-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f1536-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1536-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f1536-143">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1536-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1536-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1536-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f1536-145">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1536-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1536-146">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f1536-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f1536-147">**MRUINFOW** (Unicode) e **MRUINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f1536-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




