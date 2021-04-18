---
description: Installa un catalogo in una directory.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: InstallCatalog (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331190"
---
# <a name="installcatalog-function"></a><span data-ttu-id="43bf3-103">InstallCatalog (funzione)</span><span class="sxs-lookup"><span data-stu-id="43bf3-103">InstallCatalog function</span></span>

<span data-ttu-id="43bf3-104">\[Questa funzione non è supportata e non deve essere utilizzata.\]</span><span class="sxs-lookup"><span data-stu-id="43bf3-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="43bf3-105">Installa un catalogo in una directory.</span><span class="sxs-lookup"><span data-stu-id="43bf3-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="43bf3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43bf3-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="43bf3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="43bf3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43bf3-108">*CatalogFullPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43bf3-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43bf3-109">Puntatore a una stringa che rappresenta il percorso completo del catalogo prima dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="43bf3-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="43bf3-110">*NewBaseName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="43bf3-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43bf3-111">Puntatore al nuovo nome di base.</span><span class="sxs-lookup"><span data-stu-id="43bf3-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="43bf3-112">*NewCatalogFullPath* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="43bf3-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43bf3-113">Puntatore a una stringa che rappresenta il percorso completo del catalogo dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="43bf3-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43bf3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43bf3-114">Return value</span></span>

<span data-ttu-id="43bf3-115">Questa funzione non è attualmente implementata, quindi non restituisce un valore effettivo.</span><span class="sxs-lookup"><span data-stu-id="43bf3-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43bf3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="43bf3-116">Remarks</span></span>

<span data-ttu-id="43bf3-117">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="43bf3-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="43bf3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43bf3-118">Requirements</span></span>



| <span data-ttu-id="43bf3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43bf3-119">Requirement</span></span> | <span data-ttu-id="43bf3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="43bf3-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43bf3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="43bf3-121">DLL</span></span><br/> | <dl> <span data-ttu-id="43bf3-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43bf3-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
