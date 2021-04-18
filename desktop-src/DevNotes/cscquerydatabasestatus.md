---
description: Recupera lo stato della cache File offline.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331683"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="ea8e6-103">CSCQueryDatabaseStatus (funzione)</span><span class="sxs-lookup"><span data-stu-id="ea8e6-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="ea8e6-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="ea8e6-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="ea8e6-105">Recupera lo stato della cache File offline.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea8e6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea8e6-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="ea8e6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea8e6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8e6-108">*pulStatus*</span><span class="sxs-lookup"><span data-stu-id="ea8e6-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8e6-109">Stato.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-109">The status.</span></span> <span data-ttu-id="ea8e6-110">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ea8e6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ea8e6-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="ea8e6-112">Significato</span><span class="sxs-lookup"><span data-stu-id="ea8e6-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="ea8e6-113"><dt>**Flag \_ di 0x00000002 \_ crittografato DATABASESTATUS**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ea8e6-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="ea8e6-114">La cache è contrassegnata per la crittografia e tutti i file nella cache sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="ea8e6-115"><dt>**Flag \_ di DATABASESTATUS \_ parzialmente \_ crittografato**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ea8e6-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="ea8e6-116">La cache è contrassegnata per la crittografia, ma alcuni file nella cache non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="ea8e6-117"><dt>**Flag \_ di DATABASESTATUS \_ parzialmente non \_ crittografato**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ea8e6-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="ea8e6-118">La cache non è contrassegnata per la crittografia, ma non tutti i file nella cache sono stati decrittografati.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="ea8e6-119"><dt>**Flag \_ di 0x00000000 DATABASESTATUS non \_ crittografati**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ea8e6-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="ea8e6-120">La cache non è contrassegnata per la crittografia e tutti i file nella cache sono stati decrittografati.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="ea8e6-121">*pulErrors*</span><span class="sxs-lookup"><span data-stu-id="ea8e6-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="ea8e6-122">Questo parametro è un valore diverso da zero se si verifica un errore interno del database o 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8e6-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea8e6-123">Return value</span></span>

<span data-ttu-id="ea8e6-124">Questa funzione restituisce **true** se ha esito positivo; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea8e6-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea8e6-125">Remarks</span></span>

<span data-ttu-id="ea8e6-126">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ea8e6-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8e6-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea8e6-127">Requirements</span></span>



| <span data-ttu-id="ea8e6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea8e6-128">Requirement</span></span> | <span data-ttu-id="ea8e6-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ea8e6-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8e6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8e6-130">DLL</span></span><br/> | <dl> <span data-ttu-id="ea8e6-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8e6-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8e6-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea8e6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8e6-133">**CSCIsCSCEnabled**</span><span class="sxs-lookup"><span data-stu-id="ea8e6-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
