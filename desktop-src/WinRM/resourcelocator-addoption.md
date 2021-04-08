---
title: Metodo ResourceLocator. AddOption (WSManDisp. h)
description: Aggiunge dati aggiuntivi necessari per elaborare la richiesta. Alcuni provider WMI, ad esempio, possono richiedere un oggetto IWbemContext o SWbemNamedValueSet con informazioni specifiche del provider.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo AddOption
- Metodo AddOption Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048013"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="537e9-107">ResourceLocator. AddOption, metodo</span><span class="sxs-lookup"><span data-stu-id="537e9-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="537e9-108">Aggiunge dati aggiuntivi necessari per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="537e9-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="537e9-109">Alcuni provider WMI, ad esempio, possono richiedere un oggetto [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) con informazioni specifiche del provider.</span><span class="sxs-lookup"><span data-stu-id="537e9-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="537e9-110">È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="537e9-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="537e9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="537e9-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="537e9-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="537e9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="537e9-113">*OptionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="537e9-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="537e9-114">Nome (chiave) dell'oggetto dati facoltativo.</span><span class="sxs-lookup"><span data-stu-id="537e9-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="537e9-115">*OptionValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="537e9-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="537e9-116">Valore fornito per l'oggetto dati facoltativo.</span><span class="sxs-lookup"><span data-stu-id="537e9-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="537e9-117">*mustComply* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="537e9-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="537e9-118">Flag che indica che l'opzione deve essere elaborata.</span><span class="sxs-lookup"><span data-stu-id="537e9-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="537e9-119">Il valore predefinito è **false** (0).</span><span class="sxs-lookup"><span data-stu-id="537e9-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="537e9-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="537e9-120">Return value</span></span>

<span data-ttu-id="537e9-121">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="537e9-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="537e9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="537e9-122">Remarks</span></span>

<span data-ttu-id="537e9-123">**IWSManResourceLocator:: AddOption** è il metodo C++ corrispondente.</span><span class="sxs-lookup"><span data-stu-id="537e9-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="537e9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="537e9-124">Requirements</span></span>



| <span data-ttu-id="537e9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="537e9-125">Requirement</span></span> | <span data-ttu-id="537e9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="537e9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="537e9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="537e9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="537e9-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="537e9-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="537e9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="537e9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="537e9-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="537e9-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="537e9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="537e9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="537e9-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="537e9-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="537e9-133">IDL</span><span class="sxs-lookup"><span data-stu-id="537e9-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="537e9-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="537e9-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="537e9-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="537e9-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="537e9-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="537e9-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="537e9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="537e9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="537e9-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="537e9-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="537e9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="537e9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537e9-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="537e9-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

