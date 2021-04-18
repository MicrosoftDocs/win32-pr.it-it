---
description: Recupera il testo dalla barra del titolo della finestra specificata.
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: Funzione _GetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325692"
---
# <a name="_getwindowtext-function"></a><span data-ttu-id="dd419-103">\_GetWindowText (funzione)</span><span class="sxs-lookup"><span data-stu-id="dd419-103">\_GetWindowText function</span></span>

<span data-ttu-id="dd419-104">\[Questa funzione è un wrapper per la funzione **GetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="dd419-104">\[This function is a wrapper over the **GetWindowText** function.</span></span> <span data-ttu-id="dd419-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="dd419-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="dd419-106">Le applicazioni devono chiamare direttamente **GetWindowText** .\]</span><span class="sxs-lookup"><span data-stu-id="dd419-106">Applications should call **GetWindowText** directly.\]</span></span>

<span data-ttu-id="dd419-107">Recupera il testo dalla barra del titolo della finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="dd419-107">Retrieves the text from the specified window's title bar.</span></span> <span data-ttu-id="dd419-108">Vedere [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="dd419-108">See [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd419-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd419-109">Syntax</span></span>


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="dd419-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd419-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd419-111">*...*</span><span class="sxs-lookup"><span data-stu-id="dd419-111">*...*</span></span> 
<span data-ttu-id="dd419-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dd419-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dd419-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd419-113">Requirements</span></span>



| <span data-ttu-id="dd419-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd419-114">Requirement</span></span> | <span data-ttu-id="dd419-115">Valore</span><span class="sxs-lookup"><span data-stu-id="dd419-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd419-116">DLL</span><span class="sxs-lookup"><span data-stu-id="dd419-116">DLL</span></span><br/> | <dl> <span data-ttu-id="dd419-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd419-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd419-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd419-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd419-119">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="dd419-119">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
