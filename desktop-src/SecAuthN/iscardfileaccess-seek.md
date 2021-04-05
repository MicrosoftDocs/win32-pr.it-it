---
description: Il metodo Seek seleziona l'oggetto da cui verrà eseguito l'accesso (lettura/scrittura).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Metodo ISCardFileAccess:: Seek'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756881"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="8ca00-103">Metodo ISCardFileAccess:: Seek</span><span class="sxs-lookup"><span data-stu-id="8ca00-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="8ca00-104">\[Il metodo **Seek** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8ca00-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8ca00-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8ca00-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8ca00-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="8ca00-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8ca00-107">Il metodo **Seek** seleziona l'oggetto da cui verrà eseguito l'accesso (lettura/scrittura).</span><span class="sxs-lookup"><span data-stu-id="8ca00-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca00-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ca00-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="8ca00-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ca00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ca00-110">*hFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ca00-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca00-111">Handle del file aperto.</span><span class="sxs-lookup"><span data-stu-id="8ca00-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="8ca00-112">*Cerca* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ca00-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca00-113">Posizione in cui deve iniziare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="8ca00-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="8ca00-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca00-114">Value</span></span>                                                                                                | <span data-ttu-id="8ca00-115">Significato</span><span class="sxs-lookup"><span data-stu-id="8ca00-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="8ca00-116"><dt>SC \_ Seek \_ dall' \_ inizio</dt></span><span class="sxs-lookup"><span data-stu-id="8ca00-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="8ca00-117">Iniziare la ricerca all'inizio.</span><span class="sxs-lookup"><span data-stu-id="8ca00-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="8ca00-118"><dt>SC \_ Seek \_ dalla \_ fine </dt></span><span class="sxs-lookup"><span data-stu-id="8ca00-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="8ca00-119">Inizia la ricerca dalla fine.</span><span class="sxs-lookup"><span data-stu-id="8ca00-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="8ca00-120"><dt>SC \_ Seek \_ relativo</dt></span><span class="sxs-lookup"><span data-stu-id="8ca00-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="8ca00-121">Inizia la ricerca dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8ca00-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ca00-122">*lOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ca00-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ca00-123">Numero di oggetti dati dall'oggetto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="8ca00-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ca00-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ca00-124">Return value</span></span>

<span data-ttu-id="8ca00-125">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ca00-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8ca00-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8ca00-126">Return code</span></span>                                                                                   | <span data-ttu-id="8ca00-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ca00-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8ca00-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca00-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8ca00-129">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="8ca00-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8ca00-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca00-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8ca00-131">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="8ca00-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8ca00-132"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8ca00-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8ca00-133">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8ca00-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8ca00-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ca00-134">Remarks</span></span>

<span data-ttu-id="8ca00-135">Per leggere o scrivere da un file, chiamare rispettivamente [**Read**](iscardfileaccess-read.md) o [**Write**](iscardfileaccess-write.md) .</span><span class="sxs-lookup"><span data-stu-id="8ca00-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="8ca00-136">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="8ca00-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="8ca00-137">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="8ca00-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8ca00-138">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8ca00-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca00-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ca00-139">Requirements</span></span>



| <span data-ttu-id="8ca00-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca00-140">Requirement</span></span> | <span data-ttu-id="8ca00-141">Valore</span><span class="sxs-lookup"><span data-stu-id="8ca00-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8ca00-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca00-142">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca00-143">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8ca00-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8ca00-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8ca00-144">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca00-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ca00-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8ca00-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8ca00-146">End of client support</span></span><br/>    | <span data-ttu-id="8ca00-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8ca00-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8ca00-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="8ca00-148">End of server support</span></span><br/>    | <span data-ttu-id="8ca00-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ca00-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8ca00-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ca00-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca00-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="8ca00-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="8ca00-152">**Lettura**</span><span class="sxs-lookup"><span data-stu-id="8ca00-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="8ca00-153">**Scrittura**</span><span class="sxs-lookup"><span data-stu-id="8ca00-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
