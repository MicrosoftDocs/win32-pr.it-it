---
title: Metodo WSMan. CreateResourceLocator (WSManDisp. h)
description: Crea un oggetto ResourceLocator che può essere usato invece di specificare un URI di risorsa nelle operazioni dell'oggetto sessione, ad esempio Session. Get, Session. put o Session. enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo CreateResourceLocator
- Metodo CreateResourceLocator Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964133"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="001ba-106">WSMan. CreateResourceLocator, metodo</span><span class="sxs-lookup"><span data-stu-id="001ba-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="001ba-107">Crea un oggetto [**resourceLocator**](resourcelocator.md) che può essere usato invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="001ba-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="001ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="001ba-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="001ba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="001ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="001ba-110">*URI* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="001ba-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="001ba-111">URI di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="001ba-111">The resource URI for the resource.</span></span> <span data-ttu-id="001ba-112">Per altre informazioni sulle stringhe URI, vedere [URI di risorsa](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="001ba-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="001ba-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="001ba-113">Return value</span></span>

<span data-ttu-id="001ba-114">Oggetto [**resourceLocator**](resourcelocator.md) che può quindi essere utilizzato per eseguire operazioni WinRM locali o remote.</span><span class="sxs-lookup"><span data-stu-id="001ba-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="001ba-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="001ba-115">Remarks</span></span>

<span data-ttu-id="001ba-116">Se la proprietà **FragmentDialect** non è specificata nell'oggetto [**resourceLocator**](resourcelocator.md) , il valore predefinito è la specifica XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="001ba-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="001ba-117">Per altre informazioni, vedere [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="001ba-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="001ba-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="001ba-118">Examples</span></span>

<span data-ttu-id="001ba-119">Nell'esempio di codice VBScript seguente viene creato un oggetto [**resourceLocator**](resourcelocator.md) e viene ottenuto il valore della proprietà **Description** della scheda di rete dall'istanza di [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con indice "1".</span><span class="sxs-lookup"><span data-stu-id="001ba-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="001ba-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="001ba-120">Requirements</span></span>



| <span data-ttu-id="001ba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="001ba-121">Requirement</span></span> | <span data-ttu-id="001ba-122">Valore</span><span class="sxs-lookup"><span data-stu-id="001ba-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="001ba-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="001ba-123">Minimum supported client</span></span><br/> | <span data-ttu-id="001ba-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="001ba-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="001ba-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="001ba-125">Minimum supported server</span></span><br/> | <span data-ttu-id="001ba-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="001ba-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="001ba-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="001ba-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="001ba-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="001ba-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="001ba-129">IDL</span><span class="sxs-lookup"><span data-stu-id="001ba-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="001ba-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="001ba-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="001ba-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="001ba-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="001ba-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="001ba-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="001ba-133">DLL</span><span class="sxs-lookup"><span data-stu-id="001ba-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="001ba-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="001ba-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="001ba-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="001ba-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="001ba-136">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="001ba-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="001ba-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="001ba-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="001ba-138">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="001ba-138">**Session**</span></span>](session.md)
</dt> </dl>

 

