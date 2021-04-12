---
description: Apre il database di shim.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482893"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="d0e79-103">SdbInitDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="d0e79-103">SdbInitDatabase function</span></span>

<span data-ttu-id="d0e79-104">Apre il database di shim.</span><span class="sxs-lookup"><span data-stu-id="d0e79-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e79-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0e79-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="d0e79-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0e79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0e79-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0e79-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e79-108">Questo parametro specifica il formato del percorso nel parametro *pszDatabasePath* .</span><span class="sxs-lookup"><span data-stu-id="d0e79-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="d0e79-109">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0e79-109">It can be one of the following values.</span></span>



| <span data-ttu-id="d0e79-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d0e79-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="d0e79-111">Significato</span><span class="sxs-lookup"><span data-stu-id="d0e79-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="d0e79-112"><dt>**Nascosto \_ \_Percorsi DOS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="d0e79-113">Un percorso di stile MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="d0e79-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="d0e79-114"><dt>**Nascosto \_ DATABASE \_ FullPath**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="d0e79-115">Percorso completo.</span><span class="sxs-lookup"><span data-stu-id="d0e79-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="d0e79-116"><dt>**Nascosto \_ Nessun \_ database**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="d0e79-117">Il parametro *pszDatabasePath* viene ignorato e non viene aperto alcun database.</span><span class="sxs-lookup"><span data-stu-id="d0e79-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="d0e79-118"><dt>**Nascosto \_ \_ \_ Maschera del tipo di database**</dt> <dt>0xF00F0000</dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="d0e79-119">Questo parametro specifica un database predefinito.</span><span class="sxs-lookup"><span data-stu-id="d0e79-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="d0e79-120">Il parametro *pszDatabasePath* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d0e79-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="d0e79-121">Se *dwFlags* contiene **il \_ tipo di dati HID \_ \_ mask**, questo parametro può includere anche uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d0e79-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="d0e79-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d0e79-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="d0e79-123">Significato</span><span class="sxs-lookup"><span data-stu-id="d0e79-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="d0e79-124"><dt>**Sdb \_ 0x80030000 \_ \_ shim principale database**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="d0e79-125">Database shim applicazione.</span><span class="sxs-lookup"><span data-stu-id="d0e79-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="d0e79-126"><dt>**Sdb \_ 0x80020000 \_ \_ MSI principale del database**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="d0e79-127">Database MSI.</span><span class="sxs-lookup"><span data-stu-id="d0e79-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="d0e79-128"><dt>**Sdb \_ \_ \_ Driver principali del database**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="d0e79-129">Database di driver da bloccare.</span><span class="sxs-lookup"><span data-stu-id="d0e79-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d0e79-130">*pszDatabasePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0e79-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0e79-131">Percorso del database.</span><span class="sxs-lookup"><span data-stu-id="d0e79-131">The path to the database.</span></span> <span data-ttu-id="d0e79-132">Questo parametro può essere **null** se il parametro *dwFlags* specifica un database predefinito.</span><span class="sxs-lookup"><span data-stu-id="d0e79-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0e79-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0e79-133">Return value</span></span>

<span data-ttu-id="d0e79-134">La funzione restituisce un handle per il database aperto.</span><span class="sxs-lookup"><span data-stu-id="d0e79-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0e79-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0e79-135">Requirements</span></span>



| <span data-ttu-id="d0e79-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0e79-136">Requirement</span></span> | <span data-ttu-id="d0e79-137">Valore</span><span class="sxs-lookup"><span data-stu-id="d0e79-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0e79-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0e79-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e79-139">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d0e79-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d0e79-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0e79-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e79-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0e79-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d0e79-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d0e79-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0e79-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0e79-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0e79-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0e79-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0e79-145">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="d0e79-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="d0e79-146">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="d0e79-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="d0e79-147">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="d0e79-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="d0e79-148">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="d0e79-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




