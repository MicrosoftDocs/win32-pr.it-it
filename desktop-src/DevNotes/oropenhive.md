---
description: Carica il file hive del registro di sistema specificato in memoria e convalida l'hive.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Funzione OROpenHive (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330862"
---
# <a name="oropenhive-function"></a><span data-ttu-id="6b233-103">OROpenHive (funzione)</span><span class="sxs-lookup"><span data-stu-id="6b233-103">OROpenHive function</span></span>

<span data-ttu-id="6b233-104">Carica il file hive del registro di sistema specificato in memoria e convalida l'hive.</span><span class="sxs-lookup"><span data-stu-id="6b233-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b233-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b233-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="6b233-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b233-107">*lpHivePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b233-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b233-108">Puntatore a una stringa Unicode che specifica il nome del file hive del registro di sistema da caricare in memoria.</span><span class="sxs-lookup"><span data-stu-id="6b233-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="6b233-109">Può trattarsi di un file hive salvato con la funzione [**ORSaveHive**](orsavehive.md) o creato con la funzione [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) o [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) .</span><span class="sxs-lookup"><span data-stu-id="6b233-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="6b233-110">Il file deve avere una dimensione inferiore a 4 GB e il chiamante deve avere accesso ai \_ \_ dati di lettura del file.</span><span class="sxs-lookup"><span data-stu-id="6b233-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="6b233-111">Per ulteriori informazioni, vedere [sicurezza dei file e diritti di accesso](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="6b233-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b233-112">*phkResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6b233-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b233-113">Puntatore a una variabile che riceve un handle per la chiave radice dell'hive del registro di sistema offline caricato.</span><span class="sxs-lookup"><span data-stu-id="6b233-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="6b233-114">Se non è possibile aprire il file hive del registro di sistema o la convalida ha esito negativo, la funzione imposta questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="6b233-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b233-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b233-115">Return value</span></span>

<span data-ttu-id="6b233-116">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6b233-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="6b233-117">Se la funzione ha esito negativo, il valore restituito è un codice di errore diverso da zero definito in Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="6b233-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="6b233-118">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Per ottenere una descrizione generica dell'errore, è possibile usare la funzione FormatMessage con il valore Format Message from System flag.</span><span class="sxs-lookup"><span data-stu-id="6b233-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="6b233-119">I codici di errore possibili includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b233-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="6b233-120">Se la dimensione del file è vuota o maggiore di 4 GB, la funzione restituisce l'errore \_ BADDB.</span><span class="sxs-lookup"><span data-stu-id="6b233-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="6b233-121">Se il chiamante non dispone dei diritti di accesso necessari per aprire il file, la funzione restituisce l'errore di \_ accesso \_ negato.</span><span class="sxs-lookup"><span data-stu-id="6b233-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="6b233-122">Se la convalida dell'hive del registro di sistema non riesce, la funzione restituisce un errore \_ non il \_ file del registro \_</span><span class="sxs-lookup"><span data-stu-id="6b233-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b233-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b233-123">Remarks</span></span>

<span data-ttu-id="6b233-124">La funzione **OROpenHive** è l'unica funzione del registro di sistema offline che convalida un hive del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6b233-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="6b233-125">Se la convalida ha esito negativo, non viene effettuato alcun tentativo di ripristinare l'hive.</span><span class="sxs-lookup"><span data-stu-id="6b233-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b233-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b233-126">Requirements</span></span>



| <span data-ttu-id="6b233-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b233-127">Requirement</span></span> | <span data-ttu-id="6b233-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6b233-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b233-129">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6b233-129">Redistributable</span></span><br/> | <span data-ttu-id="6b233-130">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="6b233-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="6b233-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b233-131">Header</span></span><br/>          | <dl> <span data-ttu-id="6b233-132"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b233-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b233-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6b233-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="6b233-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b233-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b233-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b233-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b233-136">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="6b233-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="6b233-137">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="6b233-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="6b233-138">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="6b233-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="6b233-139">RegSaveKey</span><span class="sxs-lookup"><span data-stu-id="6b233-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="6b233-140">RegSaveKeyEx</span><span class="sxs-lookup"><span data-stu-id="6b233-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
