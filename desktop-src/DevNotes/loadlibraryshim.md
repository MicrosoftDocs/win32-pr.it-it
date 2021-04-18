---
description: Carica una versione specificata di una DLL della libreria .NET Framework.
ms.assetid: f001774d-ea9a-4820-aec0-99ce958b1e1d
title: LoadLibraryShim (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadLibraryShim
api_type:
- DllExport
api_location:
- Mscoree.dll
ms.openlocfilehash: 3a2fd8ab6aef8d0309748cbbf37d56ccd032b050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324696"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="25869-103">LoadLibraryShim (funzione)</span><span class="sxs-lookup"><span data-stu-id="25869-103">LoadLibraryShim function</span></span>

<span data-ttu-id="25869-104">Carica una versione specificata di una DLL della libreria .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="25869-104">Loads a specified version of a .NET Framework library DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="25869-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25869-105">Syntax</span></span>


```C++
HRESULT LoadLibraryShim(
  _In_  LPCWSTR szDllName,
  _In_  LPCWSTR szVersion,
        LPVOID  pvReserved,
  _Out_ HMODULE *phModDll
);
```



## <a name="parameters"></a><span data-ttu-id="25869-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25869-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25869-107">*szDllName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25869-107">*szDllName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25869-108">Nome della DLL da caricare dal .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="25869-108">The name of the DLL to be loaded from the .NET Framework.</span></span>

</dd> <dt>

<span data-ttu-id="25869-109">*szVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25869-109">*szVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25869-110">Versione della DLL da caricare.</span><span class="sxs-lookup"><span data-stu-id="25869-110">The version of the DLL to be loaded.</span></span> <span data-ttu-id="25869-111">Se *szVersion* è **null**, viene caricata la versione più recente della DLL specificata.</span><span class="sxs-lookup"><span data-stu-id="25869-111">If *szVersion* is **NULL**, the latest version of the specified DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="25869-112">*pvReserved*</span><span class="sxs-lookup"><span data-stu-id="25869-112">*pvReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="25869-113">Riservato.</span><span class="sxs-lookup"><span data-stu-id="25869-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="25869-114">*phModDll* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25869-114">*phModDll* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25869-115">Handle per il modulo.</span><span class="sxs-lookup"><span data-stu-id="25869-115">A handle to the module.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25869-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25869-116">Return value</span></span>

<span data-ttu-id="25869-117">Se questa funzione ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="25869-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="25869-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25869-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="25869-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="25869-119">Remarks</span></span>

<span data-ttu-id="25869-120">Questa funzione viene utilizzata per caricare le dll della libreria incluse nel pacchetto ridistribuibile .NET Framework, non nelle DLL generate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="25869-120">This function is used to load library DLLs that are included in the .NET Framework redistributable package, not user-generated DLLs.</span></span>

<span data-ttu-id="25869-121">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="25869-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="25869-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25869-122">Requirements</span></span>



| <span data-ttu-id="25869-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25869-123">Requirement</span></span> | <span data-ttu-id="25869-124">Valore</span><span class="sxs-lookup"><span data-stu-id="25869-124">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25869-125">DLL</span><span class="sxs-lookup"><span data-stu-id="25869-125">DLL</span></span><br/> | <dl> <span data-ttu-id="25869-126"><dt>Mscoree.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25869-126"><dt>Mscoree.dll</dt></span></span> </dl> |



 

 
