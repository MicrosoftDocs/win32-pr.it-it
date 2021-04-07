---
description: Il \_ Metodo Clone dell'oggetto SWbemObject restituisce un nuovo oggetto che è un clone dell'oggetto corrente.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Metodo SWbemObject.Clone_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058096"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="08cd9-103">Metodo SWbemObject. Clone \_</span><span class="sxs-lookup"><span data-stu-id="08cd9-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="08cd9-104">Il **metodo \_ Clone** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un nuovo oggetto che è un clone dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="08cd9-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="08cd9-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="08cd9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="08cd9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08cd9-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="08cd9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="08cd9-107">Parameters</span></span>

<span data-ttu-id="08cd9-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="08cd9-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08cd9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08cd9-109">Return value</span></span>

<span data-ttu-id="08cd9-110">Se ha esito positivo, questo metodo restituisce un nuovo oggetto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="08cd9-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="08cd9-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="08cd9-111">Error codes</span></span>

<span data-ttu-id="08cd9-112">Dopo il completamento del **metodo \_ Clone** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="08cd9-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="08cd9-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="08cd9-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="08cd9-114">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="08cd9-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="08cd9-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="08cd9-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="08cd9-116">Non è stato specificato **alcun** elemento come parametro e non è accettabile in questo utilizzo.</span><span class="sxs-lookup"><span data-stu-id="08cd9-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="08cd9-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="08cd9-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="08cd9-118">Memoria insufficiente per clonare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="08cd9-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08cd9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="08cd9-119">Remarks</span></span>

<span data-ttu-id="08cd9-120">Usare il **metodo \_ Clone** per duplicare una definizione di classe o un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="08cd9-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="08cd9-121">Questa operazione è utile quando è necessaria la copia originale dell'oggetto a scopo di backup mentre si modifica una nuova copia.</span><span class="sxs-lookup"><span data-stu-id="08cd9-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="08cd9-122">Analogamente, utilizzare questo metodo per creare numerose nuove istanze di da un'unica istanza di origine.</span><span class="sxs-lookup"><span data-stu-id="08cd9-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="08cd9-123">Utilizzare, ad esempio, [**SWbemObject. \_ SpawnInstance**](swbemobject-spawninstance-.md) per creare una singola istanza iniziale e utilizzare **SWbemObject. Clone \_** per produrre rapidamente 100 copie dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="08cd9-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="08cd9-124">Successivamente, è possibile modificare gli oggetti, assegnando a ognuno valori specifici.</span><span class="sxs-lookup"><span data-stu-id="08cd9-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="08cd9-125">Non è possibile usare questo metodo per convertire una definizione di classe in un'istanza o per convertire un'istanza in una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="08cd9-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="08cd9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08cd9-126">Requirements</span></span>



| <span data-ttu-id="08cd9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="08cd9-127">Requirement</span></span> | <span data-ttu-id="08cd9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="08cd9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08cd9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08cd9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="08cd9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08cd9-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08cd9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08cd9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="08cd9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08cd9-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08cd9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08cd9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="08cd9-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08cd9-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="08cd9-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="08cd9-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="08cd9-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="08cd9-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="08cd9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="08cd9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08cd9-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08cd9-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="08cd9-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="08cd9-139">CLSID</span></span><br/>                    | <span data-ttu-id="08cd9-140">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="08cd9-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="08cd9-141">IID</span><span class="sxs-lookup"><span data-stu-id="08cd9-141">IID</span></span><br/>                      | <span data-ttu-id="08cd9-142">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="08cd9-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




