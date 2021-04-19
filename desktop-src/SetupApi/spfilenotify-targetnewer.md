---
description: La \_ notifica TARGETNEWER SPFILENOTIFY viene inviata alla routine di callback se il file da copiare è stato accodato con i flag di copia SP più recenti \_ \_ o \_ forza copia SP più \_ \_ recenti specificati e una versione più recente del file esiste già nella directory di destinazione.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Messaggio SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313703"
---
# <a name="spfilenotify_targetnewer-message"></a><span data-ttu-id="841e9-103">\_Messaggio SPFILENOTIFY TARGETNEWER</span><span class="sxs-lookup"><span data-stu-id="841e9-103">SPFILENOTIFY\_TARGETNEWER message</span></span>

<span data-ttu-id="841e9-104">La **notifica \_ TARGETNEWER SPFILENOTIFY** viene inviata alla routine di callback se il file da copiare è stato accodato con i flag di copia SP più recenti \_ \_ o \_ forza copia SP più \_ \_ recenti specificati e una versione più recente del file esiste già nella directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="841e9-104">The **SPFILENOTIFY\_TARGETNEWER** notification is sent to the callback routine if the file to be copied was queued with the SP\_COPY\_NEWER or SP\_COPY\_FORCE\_NEWER flags specified and a newer version of the file already exists in the target directory.</span></span> <span data-ttu-id="841e9-105">Può essere inviato alla routine di callback da solo o ORed insieme a [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/o [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).</span><span class="sxs-lookup"><span data-stu-id="841e9-105">It can be sent to the callback routine alone or ORed together with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md) and/or [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md).</span></span>


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="841e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="841e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="841e9-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="841e9-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="841e9-108">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi per i file di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="841e9-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths for source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="841e9-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="841e9-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="841e9-110">Questo parametro non viene usato a meno che la notifica non venga combinata, usando l'operatore OR, con [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).</span><span class="sxs-lookup"><span data-stu-id="841e9-110">This parameter is not used unless this notification is combined, by using the OR operator, with [**SPFILENOTIFY\_LANGMISMATCH**](spfilenotify-langmismatch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="841e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="841e9-111">Return value</span></span>

<span data-ttu-id="841e9-112">La routine di callback deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="841e9-112">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="841e9-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="841e9-113">Return code</span></span>                                                                          | <span data-ttu-id="841e9-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="841e9-114">Description</span></span>                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="841e9-115"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="841e9-115"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="841e9-116">Sovrascrivere il file nella directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="841e9-116">Overwrite the file in the target directory.</span></span><br/> |
| <dl> <span data-ttu-id="841e9-117"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="841e9-117"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="841e9-118">Ignora l'operazione di copia corrente.</span><span class="sxs-lookup"><span data-stu-id="841e9-118">Skip the current copy operation.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="841e9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="841e9-119">Requirements</span></span>



| <span data-ttu-id="841e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="841e9-120">Requirement</span></span> | <span data-ttu-id="841e9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="841e9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="841e9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="841e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="841e9-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="841e9-123">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="841e9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="841e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="841e9-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="841e9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="841e9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="841e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="841e9-127"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="841e9-127"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841e9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="841e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841e9-129">Overview</span><span class="sxs-lookup"><span data-stu-id="841e9-129">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="841e9-130">Notifications</span><span class="sxs-lookup"><span data-stu-id="841e9-130">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="841e9-131">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="841e9-131">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="841e9-132">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="841e9-132">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="841e9-133">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="841e9-133">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="841e9-134">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="841e9-134">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="841e9-135">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="841e9-135">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="841e9-136">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="841e9-136">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




