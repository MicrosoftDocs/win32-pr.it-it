---
description: Utilizzato da un provider del servizio di crittografia (CSP) per ottenere l'handle della finestra che il CSP deve utilizzare come padre o proprietario di qualsiasi interfaccia utente visualizzata.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: Puntatore a funzione CRYPT_RETURN_HWND (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317735"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="6b26d-103">\_Puntatore a \_ funzione HWND restituito dalla crittografia</span><span class="sxs-lookup"><span data-stu-id="6b26d-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="6b26d-104">La funzione di callback **FuncReturnhWnd** viene utilizzata da un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) per ottenere l'handle della finestra che deve essere utilizzato dal CSP come padre o proprietario di qualsiasi interfaccia utente visualizzata.</span><span class="sxs-lookup"><span data-stu-id="6b26d-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b26d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b26d-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="6b26d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b26d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b26d-107">*phWnd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6b26d-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b26d-108">Indirizzo di una variabile **HWND** che riceve l'handle della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="6b26d-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b26d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b26d-109">Return value</span></span>

<span data-ttu-id="6b26d-110">Questo puntatore a funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6b26d-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b26d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b26d-111">Requirements</span></span>



| <span data-ttu-id="6b26d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b26d-112">Requirement</span></span> | <span data-ttu-id="6b26d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6b26d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b26d-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b26d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b26d-115">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b26d-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b26d-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b26d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b26d-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b26d-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6b26d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b26d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b26d-119"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b26d-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b26d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b26d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b26d-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="6b26d-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="6b26d-122">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="6b26d-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
