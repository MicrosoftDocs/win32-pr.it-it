---
description: Modifica il testo della barra del titolo della finestra specificata (se ne è presente uno).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: Funzione _SetWindowText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332237"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="e1186-103">\_SetWindowText (funzione)</span><span class="sxs-lookup"><span data-stu-id="e1186-103">\_SetWindowText function</span></span>

<span data-ttu-id="e1186-104">\[Questa funzione è un wrapper per la funzione **SetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="e1186-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="e1186-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="e1186-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="e1186-106">Le applicazioni devono chiamare direttamente **SetWindowText** .\]</span><span class="sxs-lookup"><span data-stu-id="e1186-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="e1186-107">Modifica il testo della barra del titolo della finestra specificata (se ne è presente uno).</span><span class="sxs-lookup"><span data-stu-id="e1186-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="e1186-108">Vedere [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="e1186-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="e1186-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1186-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="e1186-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1186-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1186-111">*...*</span><span class="sxs-lookup"><span data-stu-id="e1186-111">*...*</span></span> 
<span data-ttu-id="e1186-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e1186-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="e1186-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1186-113">Requirements</span></span>



| <span data-ttu-id="e1186-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1186-114">Requirement</span></span> | <span data-ttu-id="e1186-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e1186-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1186-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e1186-116">DLL</span></span><br/> | <dl> <span data-ttu-id="e1186-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1186-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1186-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1186-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1186-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="e1186-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
