---
title: Proprietà Enumerator. AtEndOfStream (WSManDisp. h)
description: Ottiene un valore booleano che indica se sono presenti altri elementi nella raccolta.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà AtEndOfStream
- Gestione remota Windows proprietà AtEndOfStream, oggetto enumeratore
- Enumeratore Gestione remota Windows oggetto, proprietà AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119371"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="0871f-106">Proprietà Enumerator. AtEndOfStream</span><span class="sxs-lookup"><span data-stu-id="0871f-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="0871f-107">Ottiene un valore booleano che indica se sono presenti altri elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="0871f-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="0871f-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0871f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0871f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0871f-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="0871f-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0871f-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="0871f-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span><span class="sxs-lookup"><span data-stu-id="0871f-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="0871f-112">Non sono presenti altri elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="0871f-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="0871f-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span><span class="sxs-lookup"><span data-stu-id="0871f-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="0871f-114">Sono disponibili altri elementi.</span><span class="sxs-lookup"><span data-stu-id="0871f-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0871f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0871f-115">Remarks</span></span>

<span data-ttu-id="0871f-116">Se si libera l'oggetto [**enumeratore**](enumerator.md) dopo avere ottenuto tutti i dati necessari, eventuali richieste di enumerazione in sospeso verranno rimosse.</span><span class="sxs-lookup"><span data-stu-id="0871f-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="0871f-117">Per ulteriori informazioni, vedere [enumerazione o visualizzazione di un elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="0871f-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0871f-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="0871f-118">Examples</span></span>

<span data-ttu-id="0871f-119">Nell'esempio VBScript seguente vengono enumerate le istanze del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0871f-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="0871f-120">Si noti che la liberazione dell'oggetto di enumerazione pulisce tutte le richieste di enumerazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0871f-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="0871f-121">La subroutine DiplayOutput formatta l'output dei dati in modo analogo allo strumento WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="0871f-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
 Dim xmlFile, xslFile
 Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
 Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
 xmlFile.LoadXml( strWinRMXml )
 xslFile.Load( "WsmTxt.xsl" )
 Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0871f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0871f-122">Requirements</span></span>



| <span data-ttu-id="0871f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0871f-123">Requirement</span></span> | <span data-ttu-id="0871f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0871f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0871f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0871f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0871f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0871f-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0871f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0871f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0871f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0871f-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0871f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0871f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0871f-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0871f-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0871f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="0871f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0871f-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0871f-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="0871f-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="0871f-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="0871f-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0871f-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0871f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0871f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0871f-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0871f-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0871f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0871f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0871f-138">**Enumeratore**</span><span class="sxs-lookup"><span data-stu-id="0871f-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="0871f-139">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="0871f-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





