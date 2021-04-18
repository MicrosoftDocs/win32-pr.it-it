---
description: La \_ notifica SPFILENOTIFY NEEDMEDIA viene inviata alla routine di callback quando è necessario un nuovo file multimediale o un nuovo file CAB.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Messaggio SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b856a95f3c2e200d1d81cfa00c05ef592c1759
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320637"
---
# <a name="spfilenotify_needmedia-message"></a><span data-ttu-id="01822-103">\_Messaggio SPFILENOTIFY NEEDMEDIA</span><span class="sxs-lookup"><span data-stu-id="01822-103">SPFILENOTIFY\_NEEDMEDIA message</span></span>

<span data-ttu-id="01822-104">La notifica **SPFILENOTIFY \_ NEEDMEDIA** viene inviata alla routine di callback quando è necessario un nuovo file multimediale o un nuovo file CAB.</span><span class="sxs-lookup"><span data-stu-id="01822-104">The **SPFILENOTIFY\_NEEDMEDIA** notification is sent to the callback routine when new media or a new cabinet file is required.</span></span>


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="01822-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="01822-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01822-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="01822-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="01822-107">Puntatore a una struttura del [**\_ supporto di origine**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .</span><span class="sxs-lookup"><span data-stu-id="01822-107">Pointer to a [**SOURCE\_MEDIA**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="01822-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="01822-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="01822-109">Puntatore a una matrice di caratteri per archiviare le nuove informazioni sul percorso fornite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="01822-109">Pointer to a character array to store new path information supplied by the user.</span></span> <span data-ttu-id="01822-110">La dimensione del buffer è una matrice **TCHAR** di \_ elementi di percorso max.</span><span class="sxs-lookup"><span data-stu-id="01822-110">The buffer size is a **TCHAR** array of MAX\_PATH elements.</span></span> <span data-ttu-id="01822-111">Le informazioni sul percorso restituite dall'applicazione di installazione non devono superare questa dimensione.</span><span class="sxs-lookup"><span data-stu-id="01822-111">The path information returned by your setup application should not exceed this size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01822-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01822-112">Return value</span></span>

<span data-ttu-id="01822-113">La routine di callback deve restituire uno dei seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="01822-113">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="01822-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="01822-114">Return code</span></span>                                                                                    | <span data-ttu-id="01822-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01822-115">Description</span></span>                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01822-116"><dt>**\_NEWPATH FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="01822-116"><dt>**FILEOP\_NEWPATH**</dt></span></span> </dl> | <span data-ttu-id="01822-117">Il supporto è presente e il file richiesto è disponibile nel percorso specificato nel buffer a cui punta *param2*.</span><span class="sxs-lookup"><span data-stu-id="01822-117">The media is present and the requested file is available at the path specified in the buffer pointed to by *Param2*.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="01822-118"><dt>**\_Ignora FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="01822-118"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="01822-119">Ignora il file richiesto</span><span class="sxs-lookup"><span data-stu-id="01822-119">Skip the requested file</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="01822-120"><dt>**\_interruzione FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="01822-120"><dt>**FILEOP\_ABORT**</dt></span></span> </dl>   | <span data-ttu-id="01822-121">Interrompi elaborazione coda.</span><span class="sxs-lookup"><span data-stu-id="01822-121">Abort queue processing.</span></span> <span data-ttu-id="01822-122">La funzione [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="01822-122">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE**.</span></span> <span data-ttu-id="01822-123">GetLastError restituisce informazioni estese sull'errore, ad esempio errore \_ annullato se l'utente è stato annullato.</span><span class="sxs-lookup"><span data-stu-id="01822-123">GetLastError returns extended error information, such as ERROR\_CANCELLED if the user canceled.</span></span><br/> |
| <dl> <span data-ttu-id="01822-124"><dt>**FILEOP-DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="01822-124"><dt>**FILEOP-DOIT**</dt></span></span> </dl>     | <span data-ttu-id="01822-125">Il supporto è disponibile.</span><span class="sxs-lookup"><span data-stu-id="01822-125">The media is available.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="01822-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01822-126">Requirements</span></span>



| <span data-ttu-id="01822-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="01822-127">Requirement</span></span> | <span data-ttu-id="01822-128">Valore</span><span class="sxs-lookup"><span data-stu-id="01822-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="01822-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01822-129">Minimum supported client</span></span><br/> | <span data-ttu-id="01822-130">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01822-130">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="01822-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01822-131">Minimum supported server</span></span><br/> | <span data-ttu-id="01822-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01822-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="01822-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01822-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="01822-134"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="01822-134"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01822-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01822-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01822-136">Overview</span><span class="sxs-lookup"><span data-stu-id="01822-136">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="01822-137">Notifications</span><span class="sxs-lookup"><span data-stu-id="01822-137">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="01822-138">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="01822-138">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="01822-139">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="01822-139">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="01822-140">**supporto di origine \_**</span><span class="sxs-lookup"><span data-stu-id="01822-140">**SOURCE\_MEDIA**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




