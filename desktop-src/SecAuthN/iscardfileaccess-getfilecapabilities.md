---
description: Il metodo GetFileCapabilities recupera un elenco di funzionalità file dal file corrente.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'Metodo ISCardFileAccess:: GetFileCapabilities'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232233"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="fb8f4-103">Metodo ISCardFileAccess:: GetFileCapabilities</span><span class="sxs-lookup"><span data-stu-id="fb8f4-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="fb8f4-104">\[Il metodo **GetFileCapabilities** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb8f4-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb8f4-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="fb8f4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="fb8f4-107">Il metodo **GetFileCapabilities** recupera un elenco di funzionalità file dal file corrente.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb8f4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb8f4-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="fb8f4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb8f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb8f4-110">*ppProperties* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fb8f4-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8f4-111">Puntatore a strutture TLV (tag, lunghezza, valore).</span><span class="sxs-lookup"><span data-stu-id="fb8f4-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="fb8f4-112">In input, questo parametro indica i file per i quali ottenere le proprietà; nell'output, questo parametro contiene le proprietà.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="fb8f4-113">L'esempio seguente è una definizione della struttura TLV.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="fb8f4-114">Per ulteriori informazioni sulle strutture TLV, vedere [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .</span><span class="sxs-lookup"><span data-stu-id="fb8f4-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="fb8f4-115">*plProperties* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fb8f4-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8f4-116">Puntatore al numero di voci TLV in *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="fb8f4-117">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb8f4-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb8f4-118">Specifica se è necessario utilizzare la messaggistica protetta e i dati preallocati.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="fb8f4-119">**\_ \_ messaggistica protetta SC \_ FL**</span><span class="sxs-lookup"><span data-stu-id="fb8f4-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="fb8f4-120">**SC \_ FL \_ allocato**</span><span class="sxs-lookup"><span data-stu-id="fb8f4-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb8f4-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb8f4-121">Return value</span></span>

<span data-ttu-id="fb8f4-122">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="fb8f4-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fb8f4-123">Return code</span></span>                                                                                   | <span data-ttu-id="fb8f4-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb8f4-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fb8f4-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f4-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb8f4-126">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="fb8f4-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f4-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="fb8f4-128">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="fb8f4-129"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f4-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fb8f4-130">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="fb8f4-131"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="fb8f4-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb8f4-132">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="fb8f4-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb8f4-133">Remarks</span></span>

<span data-ttu-id="fb8f4-134">Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="fb8f4-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="fb8f4-135">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="fb8f4-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="fb8f4-136">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="fb8f4-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb8f4-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb8f4-137">Requirements</span></span>



| <span data-ttu-id="fb8f4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb8f4-138">Requirement</span></span> | <span data-ttu-id="fb8f4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="fb8f4-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb8f4-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb8f4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fb8f4-141">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fb8f4-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fb8f4-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb8f4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fb8f4-143">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb8f4-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb8f4-144">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fb8f4-144">End of client support</span></span><br/>    | <span data-ttu-id="fb8f4-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb8f4-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="fb8f4-146">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fb8f4-146">End of server support</span></span><br/>    | <span data-ttu-id="fb8f4-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb8f4-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="fb8f4-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb8f4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb8f4-149">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="fb8f4-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
