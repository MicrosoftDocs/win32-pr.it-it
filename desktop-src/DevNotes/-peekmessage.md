---
description: Invia messaggi in ingresso inviati, controlla la coda di messaggi del thread per un messaggio inviato e recupera il messaggio (se presente).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: Funzione _PeekMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325678"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="2d49f-103">\_PeekMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d49f-103">\_PeekMessage function</span></span>

<span data-ttu-id="2d49f-104">\[Questa funzione è un wrapper per la funzione **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="2d49f-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="2d49f-105">Questa funzione può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="2d49f-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="2d49f-106">Le applicazioni devono chiamare direttamente **PeekMessage** .\]</span><span class="sxs-lookup"><span data-stu-id="2d49f-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="2d49f-107">Invia messaggi in ingresso inviati, controlla la coda di messaggi del thread per un messaggio inviato e recupera il messaggio (se presente).</span><span class="sxs-lookup"><span data-stu-id="2d49f-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="2d49f-108">Vedere [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span><span class="sxs-lookup"><span data-stu-id="2d49f-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d49f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d49f-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="2d49f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d49f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d49f-111">*...*</span><span class="sxs-lookup"><span data-stu-id="2d49f-111">*...*</span></span> 
<span data-ttu-id="2d49f-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2d49f-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2d49f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d49f-113">Requirements</span></span>



| <span data-ttu-id="2d49f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d49f-114">Requirement</span></span> | <span data-ttu-id="2d49f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2d49f-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d49f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2d49f-116">DLL</span></span><br/> | <dl> <span data-ttu-id="2d49f-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d49f-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d49f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d49f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d49f-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="2d49f-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
