---
description: La \_ notifica SPFILENOTIFY FILEINCABINET viene inviata a una routine di callback da SetupIterateCabinet per ogni file trovato nell'archivio. La routine di callback deve restituire un valore che indica se estrarre il file.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Messaggio SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318614"
---
# <a name="spfilenotify_fileincabinet-message"></a><span data-ttu-id="ddf87-104">\_Messaggio SPFILENOTIFY FILEINCABINET</span><span class="sxs-lookup"><span data-stu-id="ddf87-104">SPFILENOTIFY\_FILEINCABINET message</span></span>

<span data-ttu-id="ddf87-105">La notifica **SPFILENOTIFY \_ FILEINCABINET** viene inviata a una routine di callback da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per ogni file trovato nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="ddf87-105">The **SPFILENOTIFY\_FILEINCABINET** notification is sent to a callback routine by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) for each file found in the cabinet.</span></span> <span data-ttu-id="ddf87-106">La routine di callback deve restituire un valore che indica se estrarre il file.</span><span class="sxs-lookup"><span data-stu-id="ddf87-106">The callback routine must return a value indicating whether to extract the file.</span></span>


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a><span data-ttu-id="ddf87-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddf87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf87-108">*Param1*</span><span class="sxs-lookup"><span data-stu-id="ddf87-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="ddf87-109">Puntatore a un [**file \_ nella struttura di \_ \_ informazioni sul cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) che contiene informazioni sul file nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="ddf87-109">Pointer to a [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure that contains information about the file in the cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="ddf87-110">*Param2*</span><span class="sxs-lookup"><span data-stu-id="ddf87-110">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="ddf87-111">Puntatore a una stringa con terminazione null che contiene il nome file del file CAB.</span><span class="sxs-lookup"><span data-stu-id="ddf87-111">Pointer to a null-terminated string that contains the filename of the cabinet file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf87-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddf87-112">Return value</span></span>

<span data-ttu-id="ddf87-113">La routine di callback deve restituire uno dei seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="ddf87-113">Your callback routine should return one of the following.</span></span>



| <span data-ttu-id="ddf87-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ddf87-114">Return code</span></span>                                                                                 | <span data-ttu-id="ddf87-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddf87-115">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ddf87-116"><dt>**\_Ignora FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="ddf87-116"><dt>**FILEOP\_SKIP**</dt></span></span> </dl> | <span data-ttu-id="ddf87-117">Non estrarre il file, ignorarlo.</span><span class="sxs-lookup"><span data-stu-id="ddf87-117">Do not extract the file, skip it.</span></span><br/> |
| <dl> <span data-ttu-id="ddf87-118"><dt>**\_doit FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="ddf87-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl> | <span data-ttu-id="ddf87-119">Estrai il file.</span><span class="sxs-lookup"><span data-stu-id="ddf87-119">Extract the file.</span></span><br/>                 |



 

<span data-ttu-id="ddf87-120">Se la routine di callback restituisce FILEOP \_ doit, il nome da usare per il file estratto deve essere specificato nel membro **FullTargetName** del [**file nella struttura di \_ \_ \_ informazioni del cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) passato alla routine in *param1*.</span><span class="sxs-lookup"><span data-stu-id="ddf87-120">If your callback routine returns FILEOP\_DOIT, the name to use for the extracted file should be specified in the **FullTargetName** member of the [**FILE\_IN\_CABINET\_INFO**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) structure passed to the routine in *Param1*.</span></span>

> [!Note]  
> <span data-ttu-id="ddf87-121">Non esiste alcuna routine di callback predefinita del cabinet.</span><span class="sxs-lookup"><span data-stu-id="ddf87-121">There is no default cabinet callback routine.</span></span> <span data-ttu-id="ddf87-122">L'applicazione di installazione deve fornire una routine di callback per gestire le notifiche inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="ddf87-122">The setup application should supply a callback routine to handle the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ddf87-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddf87-123">Requirements</span></span>



| <span data-ttu-id="ddf87-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddf87-124">Requirement</span></span> | <span data-ttu-id="ddf87-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ddf87-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf87-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddf87-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ddf87-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ddf87-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ddf87-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddf87-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ddf87-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ddf87-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ddf87-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddf87-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddf87-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf87-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf87-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddf87-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf87-133">Overview</span><span class="sxs-lookup"><span data-stu-id="ddf87-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="ddf87-134">Notifications</span><span class="sxs-lookup"><span data-stu-id="ddf87-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="ddf87-135">**\_informazioni su file in \_ cabinet \_**</span><span class="sxs-lookup"><span data-stu-id="ddf87-135">**FILE\_IN\_CABINET\_INFO**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[<span data-ttu-id="ddf87-136">**SetupIterateCabinet**</span><span class="sxs-lookup"><span data-stu-id="ddf87-136">**SetupIterateCabinet**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




