---
description: Ottiene l'indirizzo di una funzione da una DLL.
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331972"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="25a9a-103">\_GetProcAddress ( \_ funzione)</span><span class="sxs-lookup"><span data-stu-id="25a9a-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="25a9a-104">\[Questa funzione è un wrapper per la funzione **GetProcAddress** .</span><span class="sxs-lookup"><span data-stu-id="25a9a-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="25a9a-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="25a9a-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="25a9a-106">Le applicazioni devono chiamare direttamente **GetProcAddress** .\]</span><span class="sxs-lookup"><span data-stu-id="25a9a-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="25a9a-107">Ottiene l'indirizzo di una funzione da una DLL.</span><span class="sxs-lookup"><span data-stu-id="25a9a-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="25a9a-108">Vedere [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="25a9a-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="25a9a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25a9a-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="25a9a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="25a9a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25a9a-111">*...*</span><span class="sxs-lookup"><span data-stu-id="25a9a-111">*...*</span></span> 
<span data-ttu-id="25a9a-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="25a9a-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="25a9a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25a9a-113">Requirements</span></span>



| <span data-ttu-id="25a9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="25a9a-114">Requirement</span></span> | <span data-ttu-id="25a9a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="25a9a-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25a9a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="25a9a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="25a9a-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25a9a-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25a9a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25a9a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25a9a-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="25a9a-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
