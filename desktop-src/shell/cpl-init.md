---
description: Inviato alla funzione CPlApplet di un'applicazione del pannello di controllo per chiedere all'utente di eseguire l'inizializzazione globale, in particolare l'allocazione della memoria.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: Messaggio CPL_INIT (cpl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f5206d773a7a0b1786b8c95104bbcf71561d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977354"
---
# <a name="cpl_init-message"></a><span data-ttu-id="a8842-103">\_Messaggio init cpl</span><span class="sxs-lookup"><span data-stu-id="a8842-103">CPL\_INIT message</span></span>

<span data-ttu-id="a8842-104">Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione del pannello di controllo per chiedere all'utente di eseguire l'inizializzazione globale, in particolare l'allocazione della memoria.</span><span class="sxs-lookup"><span data-stu-id="a8842-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to prompt it to perform global initialization, especially memory allocation.</span></span>


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a><span data-ttu-id="a8842-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8842-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8842-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8842-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a8842-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a8842-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a8842-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8842-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a8842-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a8842-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8842-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8842-110">Return value</span></span>

<span data-ttu-id="a8842-111">Se l'inizializzazione ha esito positivo, la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve restituire un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a8842-111">If initialization succeeds, the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function should return nonzero.</span></span> <span data-ttu-id="a8842-112">In caso contrario, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="a8842-112">Otherwise, it should return zero.</span></span>

<span data-ttu-id="a8842-113">Se [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) restituisce zero, l'applicazione di controllo termina la comunicazione e rilascia la DLL contenente l'applicazione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="a8842-113">If [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) returns zero, the controlling application ends communication and releases the DLL containing the Control Panel application.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8842-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8842-114">Remarks</span></span>

<span data-ttu-id="a8842-115">Poiché questo è l'unico modo in cui un'applicazione del pannello di controllo può segnalare una condizione di errore, l'applicazione deve allocare memoria in risposta a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8842-115">Because this is the only way a Control Panel application can signal an error condition, the application should allocate memory in response to this message.</span></span>

<span data-ttu-id="a8842-116">Questo messaggio viene inviato immediatamente dopo il caricamento della DLL che contiene l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8842-116">This message is sent immediately after the DLL containing the application is loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8842-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8842-117">Requirements</span></span>



| <span data-ttu-id="a8842-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8842-118">Requirement</span></span> | <span data-ttu-id="a8842-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a8842-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a8842-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8842-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a8842-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a8842-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a8842-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8842-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a8842-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a8842-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a8842-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8842-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8842-125"><dt>Cpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8842-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8842-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8842-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8842-127">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="a8842-127">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
