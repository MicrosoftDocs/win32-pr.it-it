---
description: Consente di creare un certificato utente da utilizzare con la conferenza di NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329888"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="e789c-103">NmMakeCert (funzione)</span><span class="sxs-lookup"><span data-stu-id="e789c-103">NmMakeCert function</span></span>

<span data-ttu-id="e789c-104">Consente di creare un certificato utente da utilizzare con la conferenza di NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="e789c-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e789c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e789c-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e789c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e789c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e789c-107">*szFirstName*</span><span class="sxs-lookup"><span data-stu-id="e789c-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="e789c-108">Nome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e789c-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="e789c-109">*szLastName*</span><span class="sxs-lookup"><span data-stu-id="e789c-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="e789c-110">Cognome dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e789c-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="e789c-111">*szEmailName*</span><span class="sxs-lookup"><span data-stu-id="e789c-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="e789c-112">Nome dell'indirizzo di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e789c-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="e789c-113">*szCity*</span><span class="sxs-lookup"><span data-stu-id="e789c-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="e789c-114">la città dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e789c-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="e789c-115">*szCountry*</span><span class="sxs-lookup"><span data-stu-id="e789c-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="e789c-116">Paese o area geografica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e789c-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="e789c-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="e789c-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="e789c-118">Valore che indica la modalità di creazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="e789c-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="e789c-119">I valori possibili sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e789c-119">Values can be any of the following.</span></span>



| <span data-ttu-id="e789c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e789c-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="e789c-121">Significato</span><span class="sxs-lookup"><span data-stu-id="e789c-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="e789c-122"><dt>**Nmmkcert \_ F \_ \_ solo pulizia**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="e789c-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="e789c-123">Eliminare il certificato precedente senza crearne uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="e789c-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="e789c-124"><dt>**Nmmkcert \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e789c-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="e789c-125">Eliminare il certificato precedente creato in precedenza con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e789c-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="e789c-126"><dt>**Nmmkcert \_ F \_ \_ computer locale**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="e789c-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="e789c-127">Creare il certificato nell'archivio certificati del computer locale.</span><span class="sxs-lookup"><span data-stu-id="e789c-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e789c-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e789c-128">Return value</span></span>

<span data-ttu-id="e789c-129">Restituisce 1 se la funzione ha esito positivo e-1 se la funzione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e789c-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="e789c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e789c-130">Remarks</span></span>

<span data-ttu-id="e789c-131">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e789c-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e789c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e789c-132">Requirements</span></span>



| <span data-ttu-id="e789c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e789c-133">Requirement</span></span> | <span data-ttu-id="e789c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e789c-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e789c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e789c-135">DLL</span></span><br/> | <dl> <span data-ttu-id="e789c-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e789c-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
