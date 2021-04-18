---
description: La \_ notifica FILEestrata SPFILENOTIFY viene inviata a una routine di callback da SetupIterateCabinet per indicare che un file è stato estratto dall'armadio o che un'estrazione non è riuscita e l'elaborazione del cabinet è stata annullata.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Messaggio SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efdd66c7f218e632ba817d00a6e6c9447052e350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318214"
---
# <a name="spfilenotify_fileextracted-message"></a><span data-ttu-id="8b97a-103">SPFILENOTIFY \_ messaggio FILEestraente</span><span class="sxs-lookup"><span data-stu-id="8b97a-103">SPFILENOTIFY\_FILEEXTRACTED message</span></span>

<span data-ttu-id="8b97a-104">La **notifica \_ fileestrata SPFILENOTIFY** viene inviata a una routine di callback da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per indicare che un file è stato estratto dall'armadio o che un'estrazione non è riuscita e l'elaborazione del cabinet è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="8b97a-104">The **SPFILENOTIFY\_FILEEXTRACTED** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) to indicate either that a file was extracted from the cabinet or that an extraction failed and cabinet processing has been canceled.</span></span>


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="8b97a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b97a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b97a-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="8b97a-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="8b97a-107">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sul percorso per il file estratto.</span><span class="sxs-lookup"><span data-stu-id="8b97a-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains path information for the extracted file.</span></span> <span data-ttu-id="8b97a-108">Il membro **SourceFile** della struttura **filePaths** contiene il percorso di origine completo del file CAB.</span><span class="sxs-lookup"><span data-stu-id="8b97a-108">The **SourceFile** member of the **FILEPATHS** structure contains the full source path of the cabinet.</span></span> <span data-ttu-id="8b97a-109">Il membro **TargetFile** fornisce il percorso di destinazione completo del file da installare nel sistema.</span><span class="sxs-lookup"><span data-stu-id="8b97a-109">The **TargetFile** member supplies the full target path of the file to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8b97a-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="8b97a-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="8b97a-111">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8b97a-111">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b97a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b97a-112">Return value</span></span>

<span data-ttu-id="8b97a-113">La routine di callback del cabinet deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8b97a-113">The cabinet callback routine should return one of the following values.</span></span>



| <span data-ttu-id="8b97a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b97a-114">Return code</span></span>                                                                               | <span data-ttu-id="8b97a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b97a-115">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b97a-116"><dt>**Nessun \_ errore**</dt></span><span class="sxs-lookup"><span data-stu-id="8b97a-116"><dt>**NO\_ERROR**</dt></span></span> </dl>  | <span data-ttu-id="8b97a-117">Non è stato rilevato alcun errore, continuare l'elaborazione del file CAB.</span><span class="sxs-lookup"><span data-stu-id="8b97a-117">No error was encountered, continue processing the cabinet.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="8b97a-118"><dt>**ERRORE \_ xxx**</dt></span><span class="sxs-lookup"><span data-stu-id="8b97a-118"><dt>**ERROR\_XXX**</dt></span></span> </dl> | <span data-ttu-id="8b97a-119">Si è verificato un errore del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="8b97a-119">An error of the specified type occurred.</span></span> <span data-ttu-id="8b97a-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) restituirà zero.</span><span class="sxs-lookup"><span data-stu-id="8b97a-120">[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) will return zero.</span></span> <span data-ttu-id="8b97a-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore specificato.</span><span class="sxs-lookup"><span data-stu-id="8b97a-121">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the specified error code.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="8b97a-122">Non esiste alcuna routine di callback predefinita del cabinet fornita con l'API di installazione.</span><span class="sxs-lookup"><span data-stu-id="8b97a-122">There is no default cabinet callback routine supplied with the Setup API.</span></span> <span data-ttu-id="8b97a-123">L'applicazione di installazione deve fornire una routine di callback per gestire le notifiche inviate dalla funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="8b97a-123">Your setup application should supply a callback routine to handle the notifications sent by the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8b97a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b97a-124">Requirements</span></span>



| <span data-ttu-id="8b97a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b97a-125">Requirement</span></span> | <span data-ttu-id="8b97a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8b97a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b97a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b97a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8b97a-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8b97a-128">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8b97a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b97a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8b97a-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b97a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b97a-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b97a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b97a-132"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b97a-132"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b97a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b97a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b97a-134">Overview</span><span class="sxs-lookup"><span data-stu-id="8b97a-134">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="8b97a-135">Notifications</span><span class="sxs-lookup"><span data-stu-id="8b97a-135">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="8b97a-136">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="8b97a-136">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="8b97a-137">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="8b97a-137">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

