---
description: La \_ notifica SPFILENOTIFY LANGMISMATCH viene inviata alla routine di callback se la lingua del file da copiare non corrisponde alla lingua di un file di destinazione esistente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Messaggio SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318213"
---
# <a name="spfilenotify_langmismatch-message"></a><span data-ttu-id="5a9b9-103">\_Messaggio SPFILENOTIFY LANGMISMATCH</span><span class="sxs-lookup"><span data-stu-id="5a9b9-103">SPFILENOTIFY\_LANGMISMATCH message</span></span>

<span data-ttu-id="5a9b9-104">La notifica **SPFILENOTIFY \_ LANGMISMATCH** viene inviata alla routine di callback se la lingua del file da copiare non corrisponde alla lingua di un file di destinazione esistente.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-104">The **SPFILENOTIFY\_LANGMISMATCH** notification is sent to the callback routine if the language of the file to be copied does not match the language of an existing target file.</span></span> <span data-ttu-id="5a9b9-105">Può essere inviato alla routine di callback da solo o combinato usando l'operatore OR con [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) e/o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).</span><span class="sxs-lookup"><span data-stu-id="5a9b9-105">It can be sent to the callback routine alone or combined, by using the OR operator, with [**SPFILENOTIFY\_TARGETEXISTS**](spfilenotify-targetexists.md) and/or [**SPFILENOTIFY\_TARGETNEWER**](spfilenotify-targetnewer.md).</span></span>


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a><span data-ttu-id="5a9b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a9b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a9b9-107">*Param1*</span><span class="sxs-lookup"><span data-stu-id="5a9b9-107">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9b9-108">Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi dei file di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-108">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure that contains information about the paths of the source and target files.</span></span>

</dd> <dt>

<span data-ttu-id="5a9b9-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="5a9b9-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a9b9-110">Identifica le lingue non corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-110">Identifies the mismatched languages.</span></span> <span data-ttu-id="5a9b9-111">Questo membro ha l'identificatore di lingua del file di origine nella parola bassa e l'identificatore della lingua del file di destinazione esistente nella parola alta.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-111">This member has the language identifier of the source file in the low word, and the language identifier of the existing target file in the high word.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a9b9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a9b9-112">Return value</span></span>

<span data-ttu-id="5a9b9-113">La routine di callback deve restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-113">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="5a9b9-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a9b9-114">Return code</span></span>                                                                          | <span data-ttu-id="5a9b9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a9b9-115">Description</span></span>                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a9b9-116"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="5a9b9-116"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="5a9b9-117">Copiare il file e sovrascrivere il file esistente.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-117">Copy the file and overwrite the existing file.</span></span><br/>               |
| <dl> <span data-ttu-id="5a9b9-118"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5a9b9-118"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="5a9b9-119">Ignorare l'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-119">Skip the copy operation.</span></span> <span data-ttu-id="5a9b9-120">Non sovrascrivere il file esistente.</span><span class="sxs-lookup"><span data-stu-id="5a9b9-120">Do not overwrite the existing file.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a9b9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a9b9-121">Requirements</span></span>



| <span data-ttu-id="5a9b9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a9b9-122">Requirement</span></span> | <span data-ttu-id="5a9b9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5a9b9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a9b9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a9b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5a9b9-125">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a9b9-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5a9b9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a9b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5a9b9-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a9b9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5a9b9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a9b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a9b9-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a9b9-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a9b9-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a9b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a9b9-131">Overview</span><span class="sxs-lookup"><span data-stu-id="5a9b9-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="5a9b9-132">Notifications</span><span class="sxs-lookup"><span data-stu-id="5a9b9-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="5a9b9-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="5a9b9-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="5a9b9-134">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="5a9b9-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="5a9b9-135">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="5a9b9-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[<span data-ttu-id="5a9b9-136">**SetupInstallFile**</span><span class="sxs-lookup"><span data-stu-id="5a9b9-136">**SetupInstallFile**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[<span data-ttu-id="5a9b9-137">**SetupInstallFileEx**</span><span class="sxs-lookup"><span data-stu-id="5a9b9-137">**SetupInstallFileEx**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[<span data-ttu-id="5a9b9-138">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="5a9b9-138">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




