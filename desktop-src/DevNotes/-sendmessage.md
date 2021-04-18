---
description: Invia il messaggio specificato a una finestra o a finestre.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: Funzione _SendMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325676"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="7adfd-103">\_SendMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="7adfd-103">\_SendMessage function</span></span>

<span data-ttu-id="7adfd-104">\[Questa funzione è un wrapper della funzione **SendMessage** .</span><span class="sxs-lookup"><span data-stu-id="7adfd-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="7adfd-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="7adfd-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="7adfd-106">Le applicazioni devono chiamare direttamente **SendMessage** .\]</span><span class="sxs-lookup"><span data-stu-id="7adfd-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="7adfd-107">Invia il messaggio specificato a una finestra o a finestre.</span><span class="sxs-lookup"><span data-stu-id="7adfd-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="7adfd-108">Vedere [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="7adfd-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="7adfd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7adfd-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="7adfd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7adfd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adfd-111">*...*</span><span class="sxs-lookup"><span data-stu-id="7adfd-111">*...*</span></span> 
<span data-ttu-id="7adfd-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7adfd-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7adfd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7adfd-113">Requirements</span></span>



| <span data-ttu-id="7adfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adfd-114">Requirement</span></span> | <span data-ttu-id="7adfd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7adfd-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7adfd-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7adfd-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7adfd-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adfd-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7adfd-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7adfd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adfd-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="7adfd-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
