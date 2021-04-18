---
description: Questa funzione recupera la versione della libreria del registro di sistema offline.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Funzione ORGetVersion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328366"
---
# <a name="orgetversion-function"></a><span data-ttu-id="a1dc5-103">ORGetVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1dc5-103">ORGetVersion function</span></span>

<span data-ttu-id="a1dc5-104">Questa funzione recupera la versione della libreria del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a1dc5-104">This function retrieves the version of the offline registry library.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1dc5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1dc5-105">Syntax</span></span>


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="a1dc5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1dc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1dc5-107">*pdwMajorVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1dc5-107">*pdwMajorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1dc5-108">Puntatore a una variabile per ricevere la versione principale della libreria del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a1dc5-108">A pointer to a variable to receive the major version of the offline registry library.</span></span> <span data-ttu-id="a1dc5-109">Per la versione iniziale della libreria, il valore è 1.</span><span class="sxs-lookup"><span data-stu-id="a1dc5-109">For the initial release of the library, the value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="a1dc5-110">*pdwMinorVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1dc5-110">*pdwMinorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1dc5-111">Puntatore a una variabile per ricevere la versione secondaria della libreria del registro di sistema offline.</span><span class="sxs-lookup"><span data-stu-id="a1dc5-111">A pointer to a variable to receive the minor version of the offline registry library.</span></span> <span data-ttu-id="a1dc5-112">Per la versione iniziale della libreria, il valore è 0.</span><span class="sxs-lookup"><span data-stu-id="a1dc5-112">For the initial release of the library, the value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1dc5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1dc5-113">Return value</span></span>

<span data-ttu-id="a1dc5-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a1dc5-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1dc5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1dc5-115">Requirements</span></span>



| <span data-ttu-id="a1dc5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1dc5-116">Requirement</span></span> | <span data-ttu-id="a1dc5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="a1dc5-117">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1dc5-118">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a1dc5-118">Redistributable</span></span><br/> | <span data-ttu-id="a1dc5-119">Windows offline Registry Library versione 1,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a1dc5-119">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a1dc5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1dc5-120">Header</span></span><br/>          | <dl> <span data-ttu-id="a1dc5-121"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1dc5-121"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1dc5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a1dc5-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="a1dc5-123"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1dc5-123"><dt>Offreg.dll</dt></span></span> </dl> |



 

 




