---
description: La \_ notifica TARGETEXISTS SPFILENOTIFY viene inviata alla routine di callback se il file da copiare è stato accodato con il \_ flag di copia sovrascrittura SP e il \_ file esiste già nella directory di destinazione.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Messaggio SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401756"
---
# <a name="spfilenotify_targetexists-message"></a><span data-ttu-id="9ff08-103">\_Messaggio SPFILENOTIFY TARGETEXISTS</span><span class="sxs-lookup"><span data-stu-id="9ff08-103">SPFILENOTIFY\_TARGETEXISTS message</span></span>

<span data-ttu-id="9ff08-104">La **notifica \_ TARGETEXISTS SPFILENOTIFY** viene inviata alla routine di callback se il file da copiare è stato accodato con il \_ flag di copia \_ sovrascrittura SP e il file esiste già nella directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ff08-104">The **SPFILENOTIFY\_TARGETEXISTS** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NOOVERWRITE flag and that file already exists in the target directory.</span></span> <span data-ttu-id="9ff08-105">Può essere inviato alla routine di callback da solo o combinato usando l'operatore OR con le notifiche [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff08-105">It can be sent to the callback routine alone or combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md) notifications.</span></span>


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="9ff08-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ff08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ff08-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="9ff08-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff08-108">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi per i file di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ff08-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="9ff08-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="9ff08-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="9ff08-110">Questo parametro non viene usato a meno che la notifica non venga combinata, usando l'operatore OR, con la notifica [**\_ LANGMISMATCH di SPFILENOTIFY**](spfilenotify-langmismatch.md) .</span><span class="sxs-lookup"><span data-stu-id="9ff08-110">This parameter is not used unless this notification is combined, by using the OR operator, with the [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ff08-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ff08-111">Return value</span></span>

<span data-ttu-id="9ff08-112">La routine di callback deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ff08-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="9ff08-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9ff08-113">Return code</span></span>                                                                          | <span data-ttu-id="9ff08-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ff08-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="9ff08-115"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff08-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="9ff08-116">Sovrascrivere il file nella directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ff08-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="9ff08-117"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="9ff08-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="9ff08-118">Ignora l'operazione di copia corrente.</span><span class="sxs-lookup"><span data-stu-id="9ff08-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="9ff08-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ff08-119">Requirements</span></span>



| <span data-ttu-id="9ff08-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ff08-120">Requirement</span></span> | <span data-ttu-id="9ff08-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9ff08-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff08-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ff08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff08-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9ff08-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9ff08-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ff08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff08-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ff08-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ff08-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ff08-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff08-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ff08-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff08-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ff08-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff08-129">Overview</span><span class="sxs-lookup"><span data-stu-id="9ff08-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="9ff08-130">Notifications</span><span class="sxs-lookup"><span data-stu-id="9ff08-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="9ff08-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="9ff08-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="9ff08-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="9ff08-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="9ff08-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="9ff08-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="9ff08-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="9ff08-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="9ff08-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="9ff08-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="9ff08-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="9ff08-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




