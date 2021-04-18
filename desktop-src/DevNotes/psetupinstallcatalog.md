---
description: Installa un file di catalogo.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: pSetupInstallCatalog (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330418"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="7d0df-103">pSetupInstallCatalog (funzione)</span><span class="sxs-lookup"><span data-stu-id="7d0df-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="7d0df-104">\[Questa funzione non è più supportata da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d0df-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="7d0df-105">Gli sviluppatori devono usare **CryptCATAdminAddCatalog**.\]</span><span class="sxs-lookup"><span data-stu-id="7d0df-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="7d0df-106">Installa un file di catalogo.</span><span class="sxs-lookup"><span data-stu-id="7d0df-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d0df-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d0df-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="7d0df-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d0df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d0df-109">*CatalogFullPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d0df-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d0df-110">Percorso completo del catalogo da installare nel sistema.</span><span class="sxs-lookup"><span data-stu-id="7d0df-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7d0df-111">*NewBaseName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d0df-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d0df-112">Nuovo nome di base da utilizzare quando il file di catalogo viene copiato nell'archivio del catalogo.</span><span class="sxs-lookup"><span data-stu-id="7d0df-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="7d0df-113">*NewCatalogFullPath* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7d0df-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d0df-114">Riceve facoltativamente il percorso completo del file di catalogo nell'archivio del catalogo.</span><span class="sxs-lookup"><span data-stu-id="7d0df-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="7d0df-115">Questo buffer deve essere almeno il **numero \_ massimo** di byte di percorso (versione ANSI) o chars (versione Unicode).</span><span class="sxs-lookup"><span data-stu-id="7d0df-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d0df-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d0df-116">Return value</span></span>

<span data-ttu-id="7d0df-117">Se la funzione ha esito positivo, non viene restituito **alcun \_ errore**. in caso contrario, restituisce un codice di errore Win32 che indica la motivo dell'errore.</span><span class="sxs-lookup"><span data-stu-id="7d0df-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d0df-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d0df-118">Remarks</span></span>

<span data-ttu-id="7d0df-119">Il file viene copiato dal sistema in una directory speciale ed eventualmente rinominato.</span><span class="sxs-lookup"><span data-stu-id="7d0df-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="7d0df-120">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7d0df-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d0df-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d0df-121">Requirements</span></span>



| <span data-ttu-id="7d0df-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d0df-122">Requirement</span></span> | <span data-ttu-id="7d0df-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7d0df-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0df-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7d0df-124">DLL</span></span><br/> | <dl> <span data-ttu-id="7d0df-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d0df-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d0df-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d0df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0df-127">**CryptCATAdminAddCatalog**</span><span class="sxs-lookup"><span data-stu-id="7d0df-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
