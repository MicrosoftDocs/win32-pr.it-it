---
description: Il \_ Metodo Clone dell'oggetto SWbemLastError restituisce un nuovo oggetto che è un clone dell'oggetto SWbemLastError corrente.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Metodo SWbemLastError.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314568"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="c37f4-103">Metodo SWbemLastError. Clone \_</span><span class="sxs-lookup"><span data-stu-id="c37f4-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="c37f4-104">Il **metodo \_ Clone** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un nuovo oggetto che è un clone dell'oggetto **SWbemLastError** corrente.</span><span class="sxs-lookup"><span data-stu-id="c37f4-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="c37f4-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c37f4-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c37f4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c37f4-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="c37f4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c37f4-107">Parameters</span></span>

<span data-ttu-id="c37f4-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c37f4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c37f4-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c37f4-109">Return value</span></span>

<span data-ttu-id="c37f4-110">Se il **metodo \_ Clone** ha esito positivo, restituisce un nuovo oggetto [**SWbemLastError**](swbemlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c37f4-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c37f4-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c37f4-111">Error codes</span></span>

<span data-ttu-id="c37f4-112">Al termine del metodo **Clone \_** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="c37f4-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="c37f4-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c37f4-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c37f4-114">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c37f4-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="c37f4-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c37f4-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c37f4-116">Parametro specificato non valido.</span><span class="sxs-lookup"><span data-stu-id="c37f4-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c37f4-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c37f4-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c37f4-118">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c37f4-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c37f4-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c37f4-119">Remarks</span></span>

<span data-ttu-id="c37f4-120">Usare il **metodo \_ Clone** per duplicare una definizione di classe o un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="c37f4-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="c37f4-121">Questo metodo è utile quando è necessario eseguire il backup della copia originale dell'oggetto durante la modifica di una nuova copia.</span><span class="sxs-lookup"><span data-stu-id="c37f4-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="c37f4-122">Usare inoltre questo metodo per creare molte nuove istanze di da un'unica istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="c37f4-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="c37f4-123">Utilizzare, ad esempio, [**SWbemObject. \_ SpawnInstance**](swbemobject-spawninstance-.md) per creare una singola istanza iniziale e utilizzare **SWbemLastError. \_ Clone** per produrre rapidamente 100 copie dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c37f4-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="c37f4-124">Successivamente, è possibile modificare gli oggetti, fornendo valori specifici per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="c37f4-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="c37f4-125">Non è possibile utilizzare questo metodo per convertire una definizione di classe in un'istanza o per convertire un'istanza in una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="c37f4-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="c37f4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c37f4-126">Requirements</span></span>



| <span data-ttu-id="c37f4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c37f4-127">Requirement</span></span> | <span data-ttu-id="c37f4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c37f4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c37f4-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c37f4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c37f4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c37f4-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c37f4-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c37f4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c37f4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c37f4-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c37f4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c37f4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c37f4-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c37f4-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c37f4-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c37f4-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="c37f4-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c37f4-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c37f4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c37f4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c37f4-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c37f4-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c37f4-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="c37f4-139">CLSID</span></span><br/>                    | <span data-ttu-id="c37f4-140">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="c37f4-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="c37f4-141">IID</span><span class="sxs-lookup"><span data-stu-id="c37f4-141">IID</span></span><br/>                      | <span data-ttu-id="c37f4-142">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="c37f4-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




