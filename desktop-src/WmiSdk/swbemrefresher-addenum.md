---
description: Aggiunge un nuovo enumeratore all'oggetto SWbemRefresher. Questo enumeratore è per tutte le istanze della classe specificata nel parametro strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. AddEnum (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761399"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="e433e-104">SWbemRefresher. AddEnum, metodo</span><span class="sxs-lookup"><span data-stu-id="e433e-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="e433e-105">Il metodo **SWbemRefresher. AddEnum** aggiunge un nuovo enumeratore all'oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="e433e-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="e433e-106">Questo enumeratore è per tutte le istanze della classe specificata nel parametro *strClass* .</span><span class="sxs-lookup"><span data-stu-id="e433e-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="e433e-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e433e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e433e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e433e-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e433e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e433e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e433e-110">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="e433e-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="e433e-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e433e-111">Required.</span></span> <span data-ttu-id="e433e-112">Oggetto [**SWbemServices**](swbemservices.md) che rappresenta una connessione allo spazio dei nomi in cui risiede l'oggetto da aggiungere all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e433e-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="e433e-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="e433e-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="e433e-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e433e-114">Required.</span></span> <span data-ttu-id="e433e-115">Stringa che contiene la classe che viene aggiunta all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e433e-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="e433e-116">Questa classe viene utilizzata come enumeratore delle istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="e433e-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="e433e-117">La proprietà [**index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) restituito rappresenta l'indice dell'enumeratore nella raccolta di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="e433e-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="e433e-118">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="e433e-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e433e-119">Stringa che contiene il percorso dell'oggetto per il quale viene eseguito il metodo.</span><span class="sxs-lookup"><span data-stu-id="e433e-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="e433e-120">*objWbemNamedvalueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="e433e-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e433e-121">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="e433e-121">Typically, this is undefined.</span></span> <span data-ttu-id="e433e-122">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="e433e-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="e433e-123">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="e433e-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e433e-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e433e-124">Return value</span></span>

<span data-ttu-id="e433e-125">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) che contiene un enumeratore per tutte le istanze della classe specificata.</span><span class="sxs-lookup"><span data-stu-id="e433e-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e433e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e433e-126">Requirements</span></span>



| <span data-ttu-id="e433e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e433e-127">Requirement</span></span> | <span data-ttu-id="e433e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e433e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e433e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e433e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e433e-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e433e-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e433e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e433e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e433e-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e433e-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e433e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e433e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e433e-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e433e-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e433e-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e433e-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="e433e-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e433e-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e433e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e433e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e433e-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e433e-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e433e-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="e433e-139">CLSID</span></span><br/>                    | <span data-ttu-id="e433e-140">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="e433e-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="e433e-141">IID</span><span class="sxs-lookup"><span data-stu-id="e433e-141">IID</span></span><br/>                      | <span data-ttu-id="e433e-142">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="e433e-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="e433e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e433e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e433e-144">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="e433e-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




