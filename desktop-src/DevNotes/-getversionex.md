---
description: Ottiene informazioni sulla versione del sistema operativo.
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: Funzione _GetVersionEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325693"
---
# <a name="_getversionex-function"></a><span data-ttu-id="403b3-103">\_GetVersionEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="403b3-103">\_GetVersionEx function</span></span>

<span data-ttu-id="403b3-104">\[Questa funzione è un wrapper per la funzione **GetVersionEx** .</span><span class="sxs-lookup"><span data-stu-id="403b3-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="403b3-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="403b3-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="403b3-106">Le applicazioni devono chiamare direttamente **GetVersionEx** .\]</span><span class="sxs-lookup"><span data-stu-id="403b3-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="403b3-107">Ottiene informazioni sulla versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="403b3-107">Gets information about the operating system version.</span></span> <span data-ttu-id="403b3-108">Vedere [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span><span class="sxs-lookup"><span data-stu-id="403b3-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="403b3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="403b3-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="403b3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="403b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403b3-111">*...*</span><span class="sxs-lookup"><span data-stu-id="403b3-111">*...*</span></span> 
<span data-ttu-id="403b3-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="403b3-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="403b3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="403b3-113">Requirements</span></span>



| <span data-ttu-id="403b3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="403b3-114">Requirement</span></span> | <span data-ttu-id="403b3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="403b3-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="403b3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="403b3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="403b3-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="403b3-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="403b3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="403b3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403b3-119">**GetVersionEx**</span><span class="sxs-lookup"><span data-stu-id="403b3-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
