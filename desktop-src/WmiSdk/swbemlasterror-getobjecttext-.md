---
description: Il \_ metodo GetObjectText dell'oggetto SWbemLastError restituisce un rendering testuale dell'oggetto in un formato di Managed Object Format (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Metodo SWbemLastError.GetObjectText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967659"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="7f6c2-103">SWbemLastError. GetObjectText, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="7f6c2-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="7f6c2-104">Il **metodo \_ GetObjectText** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un rendering testuale dell'oggetto in un formato di [Managed Object Format (MOF)](managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="7f6c2-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="7f6c2-105">Questo oggetto MOF può essere utilizzato per visualizzare il contenuto di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="7f6c2-106">Si noti che il testo MOF restituito non contiene tutte le informazioni sull'oggetto, ma solo le informazioni sufficienti per consentire al compilatore MOF di ricreare l'oggetto originale.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="7f6c2-107">Ad esempio, non vengono trovate informazioni sui qualificatori propagati o sulle proprietà della classe padre.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="7f6c2-108">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7f6c2-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6c2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f6c2-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7f6c2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f6c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f6c2-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7f6c2-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7f6c2-112">Questo parametro è riservato e deve essere 0 (zero) se specificato.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f6c2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f6c2-113">Return value</span></span>

<span data-ttu-id="7f6c2-114">Se ha esito positivo, questo metodo restituisce una stringa che contiene il testo di output.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f6c2-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7f6c2-115">Error codes</span></span>

<span data-ttu-id="7f6c2-116">Al termine del metodo **GetObjectText \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7f6c2-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7f6c2-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7f6c2-118">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c2-119">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7f6c2-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7f6c2-120">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7f6c2-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7f6c2-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7f6c2-122">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7f6c2-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f6c2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f6c2-123">Requirements</span></span>



| <span data-ttu-id="7f6c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f6c2-124">Requirement</span></span> | <span data-ttu-id="7f6c2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7f6c2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6c2-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f6c2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6c2-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f6c2-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f6c2-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f6c2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6c2-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f6c2-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f6c2-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f6c2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f6c2-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c2-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f6c2-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7f6c2-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f6c2-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c2-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7f6c2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6c2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f6c2-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6c2-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f6c2-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="7f6c2-136">CLSID</span></span><br/>                    | <span data-ttu-id="7f6c2-137">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="7f6c2-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="7f6c2-138">IID</span><span class="sxs-lookup"><span data-stu-id="7f6c2-138">IID</span></span><br/>                      | <span data-ttu-id="7f6c2-139">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="7f6c2-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




