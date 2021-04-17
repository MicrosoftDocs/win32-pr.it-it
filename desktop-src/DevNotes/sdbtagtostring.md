---
description: Recupera il nome visualizzato del TAG specificato.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: SdbTagToString (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483124"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="23b43-103">SdbTagToString (funzione)</span><span class="sxs-lookup"><span data-stu-id="23b43-103">SdbTagToString function</span></span>

<span data-ttu-id="23b43-104">Recupera il nome visualizzato del TAG specificato.</span><span class="sxs-lookup"><span data-stu-id="23b43-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b43-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23b43-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="23b43-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23b43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b43-107">*tag* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="23b43-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23b43-108">TAG.</span><span class="sxs-lookup"><span data-stu-id="23b43-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b43-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23b43-109">Return value</span></span>

<span data-ttu-id="23b43-110">La funzione restituisce un puntatore alla stringa con terminazione null o a "InvalidTag".</span><span class="sxs-lookup"><span data-stu-id="23b43-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="23b43-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23b43-111">Requirements</span></span>



| <span data-ttu-id="23b43-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="23b43-112">Requirement</span></span> | <span data-ttu-id="23b43-113">Valore</span><span class="sxs-lookup"><span data-stu-id="23b43-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23b43-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23b43-114">Minimum supported client</span></span><br/> | <span data-ttu-id="23b43-115">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="23b43-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="23b43-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23b43-116">Minimum supported server</span></span><br/> | <span data-ttu-id="23b43-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23b43-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23b43-118">DLL</span><span class="sxs-lookup"><span data-stu-id="23b43-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b43-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b43-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b43-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23b43-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b43-121">**TAG**</span><span class="sxs-lookup"><span data-stu-id="23b43-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 




