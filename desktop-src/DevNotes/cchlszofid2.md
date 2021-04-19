---
description: Decodifica e archivia una stringa.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331472"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="850a1-103">CchLszOfId2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="850a1-103">CchLszOfId2 function</span></span>

<span data-ttu-id="850a1-104">Decodifica e archivia una stringa.</span><span class="sxs-lookup"><span data-stu-id="850a1-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="850a1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="850a1-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="850a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="850a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="850a1-107">*id*</span><span class="sxs-lookup"><span data-stu-id="850a1-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="850a1-108">Identificatore della stringa nel file di risorse da decodificare e archiviare.</span><span class="sxs-lookup"><span data-stu-id="850a1-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="850a1-109">La validità della stringa non viene verificata.</span><span class="sxs-lookup"><span data-stu-id="850a1-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="850a1-110">*LSZ*</span><span class="sxs-lookup"><span data-stu-id="850a1-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="850a1-111">Puntatore a un buffer con una lunghezza di *cbmax*.</span><span class="sxs-lookup"><span data-stu-id="850a1-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="850a1-112">Le stringhe più lunghe di *cbmax* vengono troncate.</span><span class="sxs-lookup"><span data-stu-id="850a1-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="850a1-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="850a1-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="850a1-114">Lunghezza massima della stringa da archiviare nel parametro *LSZ* .</span><span class="sxs-lookup"><span data-stu-id="850a1-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="850a1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="850a1-115">Return value</span></span>

<span data-ttu-id="850a1-116">Questa funzione restituisce la stringa decodificata.</span><span class="sxs-lookup"><span data-stu-id="850a1-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="850a1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="850a1-117">Remarks</span></span>

<span data-ttu-id="850a1-118">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="850a1-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="850a1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="850a1-119">Requirements</span></span>



| <span data-ttu-id="850a1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="850a1-120">Requirement</span></span> | <span data-ttu-id="850a1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="850a1-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="850a1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="850a1-122">DLL</span></span><br/> | <dl> <span data-ttu-id="850a1-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="850a1-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
