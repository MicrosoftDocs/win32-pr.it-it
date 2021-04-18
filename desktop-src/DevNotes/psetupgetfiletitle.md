---
description: Recupera il titolo del file per il percorso del file specificato.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: pSetupGetFileTitle (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325097"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="e83aa-103">pSetupGetFileTitle (funzione)</span><span class="sxs-lookup"><span data-stu-id="e83aa-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="e83aa-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="e83aa-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="e83aa-105">Recupera il titolo del file per il percorso del file specificato.</span><span class="sxs-lookup"><span data-stu-id="e83aa-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="e83aa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e83aa-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="e83aa-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e83aa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e83aa-108">*FilePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e83aa-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e83aa-109">Percorso del file.</span><span class="sxs-lookup"><span data-stu-id="e83aa-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e83aa-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e83aa-110">Return value</span></span>

<span data-ttu-id="e83aa-111">Puntatore a una stringa che riceve il titolo del file.</span><span class="sxs-lookup"><span data-stu-id="e83aa-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="e83aa-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e83aa-112">Remarks</span></span>

<span data-ttu-id="e83aa-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e83aa-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83aa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e83aa-114">Requirements</span></span>



| <span data-ttu-id="e83aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e83aa-115">Requirement</span></span> | <span data-ttu-id="e83aa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e83aa-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e83aa-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e83aa-117">DLL</span></span><br/> | <dl> <span data-ttu-id="e83aa-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e83aa-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
