---
description: Il metodo SWbemRefresher. Add aggiunge un nuovo oggetto SWbemRefreshableItem alla raccolta nell'oggetto SWbemRefresher. Oggetto SWbemRefreshableItem alla raccolta nell'oggetto SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320541"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="0b59d-103">SWbemRefresher. Add, metodo</span><span class="sxs-lookup"><span data-stu-id="0b59d-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="0b59d-104">Il metodo **SWbemRefresher. Add** aggiunge un nuovo oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) alla raccolta nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="0b59d-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="0b59d-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0b59d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b59d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b59d-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0b59d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b59d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b59d-108">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="0b59d-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="0b59d-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b59d-109">Required.</span></span> <span data-ttu-id="0b59d-110">Oggetto [**SWbemServices**](swbemservices.md) che rappresenta una connessione allo spazio dei nomi in cui risiede l'oggetto da aggiungere all'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0b59d-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="0b59d-111">*strInstancePath*</span><span class="sxs-lookup"><span data-stu-id="0b59d-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0b59d-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0b59d-112">Required.</span></span> <span data-ttu-id="0b59d-113">Stringa che contiene il percorso relativo dell'oggetto nello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0b59d-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="0b59d-114">Il percorso deve contenere un'istanza.</span><span class="sxs-lookup"><span data-stu-id="0b59d-114">The path must contain an instance.</span></span> <span data-ttu-id="0b59d-115">La proprietà [**index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) restituito rappresenta l'indice dell'oggetto nella raccolta di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="0b59d-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="0b59d-116">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="0b59d-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b59d-117">Stringa che contiene il percorso dell'oggetto per il quale viene eseguito il metodo.</span><span class="sxs-lookup"><span data-stu-id="0b59d-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="0b59d-118">*objWbemNamedvalueSet* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="0b59d-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0b59d-119">In genere, non è definito.</span><span class="sxs-lookup"><span data-stu-id="0b59d-119">Typically, this is undefined.</span></span> <span data-ttu-id="0b59d-120">In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0b59d-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="0b59d-121">Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.</span><span class="sxs-lookup"><span data-stu-id="0b59d-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b59d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b59d-122">Return value</span></span>

<span data-ttu-id="0b59d-123">Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) che contiene un singolo oggetto aggiornabile.</span><span class="sxs-lookup"><span data-stu-id="0b59d-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b59d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b59d-124">Requirements</span></span>



| <span data-ttu-id="0b59d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b59d-125">Requirement</span></span> | <span data-ttu-id="0b59d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0b59d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b59d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b59d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b59d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b59d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b59d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b59d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b59d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b59d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b59d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b59d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b59d-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b59d-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0b59d-133">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0b59d-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b59d-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0b59d-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0b59d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0b59d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b59d-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b59d-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b59d-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="0b59d-137">CLSID</span></span><br/>                    | <span data-ttu-id="0b59d-138">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="0b59d-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="0b59d-139">IID</span><span class="sxs-lookup"><span data-stu-id="0b59d-139">IID</span></span><br/>                      | <span data-ttu-id="0b59d-140">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="0b59d-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="0b59d-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b59d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b59d-142">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="0b59d-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




