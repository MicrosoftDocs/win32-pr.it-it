---
description: La \_ notifica SPFILENOTIFY NEEDNEWCABINET viene inviata da SetupIterateCabinet per indicare che il file corrente continua in un altro file CAB.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Messaggio SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233679"
---
# <a name="spfilenotify_neednewcabinet-message"></a><span data-ttu-id="b5f39-103">\_Messaggio SPFILENOTIFY NEEDNEWCABINET</span><span class="sxs-lookup"><span data-stu-id="b5f39-103">SPFILENOTIFY\_NEEDNEWCABINET message</span></span>

<span data-ttu-id="b5f39-104">La notifica **SPFILENOTIFY \_ NEEDNEWCABINET** viene inviata da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per indicare che il file corrente continua in un altro file CAB.</span><span class="sxs-lookup"><span data-stu-id="b5f39-104">The **SPFILENOTIFY\_NEEDNEWCABINET** notification is sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate that the current file continues in another cabinet.</span></span> <span data-ttu-id="b5f39-105">La routine di callback può quindi chiamare [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)o creare la propria finestra di dialogo per richiedere all'utente di inserire il disco successivo.</span><span class="sxs-lookup"><span data-stu-id="b5f39-105">Your callback routine can then call [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), or create its own dialog box to prompt the user to insert the next disk.</span></span>


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a><span data-ttu-id="b5f39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5f39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f39-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="b5f39-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f39-108">Puntatore a una struttura di [**\_ informazioni sul cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) che contiene informazioni sul file CAB e il file da estrarre.</span><span class="sxs-lookup"><span data-stu-id="b5f39-108">Pointer to a [**CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) structure that contains information about the cabinet and the file to be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="b5f39-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="b5f39-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f39-110">Se il callback non restituisce alcun \_ errore, questo parametro è un puntatore a una stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="b5f39-110">If the callback returns NO\_ERROR, this parameter is a pointer to a null-terminated string.</span></span> <span data-ttu-id="b5f39-111">Se la stringa non è vuota, specifica un nuovo percorso per il file CAB.</span><span class="sxs-lookup"><span data-stu-id="b5f39-111">If the string is not empty, it specifies a new path to the cabinet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f39-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5f39-112">Return value</span></span>

<span data-ttu-id="b5f39-113">La routine deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5f39-113">Your routine should return one of the following values.</span></span>



| <span data-ttu-id="b5f39-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b5f39-114">Return code</span></span>                                                                                 | <span data-ttu-id="b5f39-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5f39-115">Description</span></span>                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5f39-116"><dt>**Nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f39-116"><dt>**NO\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="b5f39-117">Non è stato rilevato alcun errore, continuare l'elaborazione del file CAB.</span><span class="sxs-lookup"><span data-stu-id="b5f39-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="b5f39-118"><dt>\**Errore \_* XXX \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b5f39-118"><dt>\**ERROR\_* XXX\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b5f39-119">Si è verificato un errore del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="b5f39-119">An error of the specified type occurred.</span></span> <span data-ttu-id="b5f39-120">La funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) restituirà **false** e il codice di errore specificato verrà restituito da una chiamata a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b5f39-120">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="b5f39-121">Non esiste alcuna routine di callback predefinita del cabinet. Pertanto, è necessario fornire una routine di callback per gestire le notifiche inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="b5f39-121">There is no default cabinet callback routine; thus, you must supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="remarks"></a><span data-ttu-id="b5f39-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5f39-122">Remarks</span></span>

<span data-ttu-id="b5f39-123">Se la routine di callback non restituisce alcun \_ errore, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) controlla il buffer a cui punta *param2*.</span><span class="sxs-lookup"><span data-stu-id="b5f39-123">If the callback routine returns NO\_ERROR, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) checks the buffer pointed to by *Param2*.</span></span> <span data-ttu-id="b5f39-124">Se il buffer non è vuoto, contiene un nuovo percorso di origine.</span><span class="sxs-lookup"><span data-stu-id="b5f39-124">If the buffer is not empty, then it contains a new source path.</span></span> <span data-ttu-id="b5f39-125">Se il buffer è vuoto, si presuppone che il percorso di origine sia invariato.</span><span class="sxs-lookup"><span data-stu-id="b5f39-125">If the buffer is empty, the source path is assumed to be unchanged.</span></span>

<span data-ttu-id="b5f39-126">La funzione di callback deve garantire che il file CAB sia accessibile prima che venga restituito, chiamando la funzione [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , se è necessario inserire nuovi supporti.</span><span class="sxs-lookup"><span data-stu-id="b5f39-126">Your callback function should ensure that the cabinet is accessible before it returns, calling the [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) function, if new media needs to be inserted.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f39-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5f39-127">Requirements</span></span>



| <span data-ttu-id="b5f39-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f39-128">Requirement</span></span> | <span data-ttu-id="b5f39-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b5f39-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f39-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5f39-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b5f39-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b5f39-131">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b5f39-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5f39-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b5f39-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5f39-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5f39-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5f39-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5f39-135"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f39-135"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f39-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5f39-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f39-137">Overview</span><span class="sxs-lookup"><span data-stu-id="b5f39-137">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="b5f39-138">Notifications</span><span class="sxs-lookup"><span data-stu-id="b5f39-138">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="b5f39-139">**informazioni sul CABINET \_**</span><span class="sxs-lookup"><span data-stu-id="b5f39-139">**CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="b5f39-140">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="b5f39-140">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

