---
description: 'Funzione pSetupStringTableInitializeEx: inizializza una tabella di stringhe.'
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: Funzione pSetupStringTableInitializeEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 78ee96e7e366fdff821e8202300ff28de0a14af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096649"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="3d2d7-103">Funzione pSetupStringTableInitializeEx</span><span class="sxs-lookup"><span data-stu-id="3d2d7-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="3d2d7-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="3d2d7-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="3d2d7-105">Inizializza una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="3d2d7-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2d7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d2d7-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="3d2d7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d2d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d2d7-108">*ExtraDataSize* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3d2d7-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2d7-109">Dimensioni dell'oggetto dati aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="3d2d7-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="3d2d7-110">*Riservato* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3d2d7-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d2d7-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3d2d7-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d2d7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d2d7-112">Remarks</span></span>

<span data-ttu-id="3d2d7-113">A questa funzione non è associata alcuna libreria di importazione o file di intestazione. è necessario chiamarlo usando le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)</span><span class="sxs-lookup"><span data-stu-id="3d2d7-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2d7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d2d7-114">Requirements</span></span>



| <span data-ttu-id="3d2d7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d2d7-115">Requirement</span></span> | <span data-ttu-id="3d2d7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3d2d7-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2d7-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3d2d7-117">DLL</span></span><br/> | <dl> <span data-ttu-id="3d2d7-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d2d7-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
