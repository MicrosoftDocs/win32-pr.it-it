---
title: Metodo Enumerator. ReadItem (WSManDisp. h)
description: Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo ReadItem
- Metodo ReadItem Gestione remota Windows, oggetto Enumerator
- Enumeratore Gestione remota Windows oggetto, metodo ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048136"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="7485f-106">Enumerator. ReadItem, metodo</span><span class="sxs-lookup"><span data-stu-id="7485f-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="7485f-107">Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7485f-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="7485f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7485f-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="7485f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7485f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7485f-110">*risorse*</span><span class="sxs-lookup"><span data-stu-id="7485f-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="7485f-111">URI dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7485f-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7485f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7485f-112">Return value</span></span>

<span data-ttu-id="7485f-113">Rappresentazione XML dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7485f-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="7485f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7485f-114">Remarks</span></span>

<span data-ttu-id="7485f-115">Per limitare il numero di elementi letti, impostare la proprietà [**Session.BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="7485f-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="7485f-116">Si noti che la liberazione dell'oggetto di enumerazione pulisce tutte le richieste di enumerazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7485f-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="7485f-117">Il metodo [**Session. enumerate**](session-enumerate.md) non ottiene una raccolta nello stesso modo in cui una [query WMI](/windows/desktop/WmiSdk/querying-wmi), ad esempio `SELECT * from Win32_LogicalDisk` , restituisce una raccolta in un [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span><span class="sxs-lookup"><span data-stu-id="7485f-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="7485f-118">Per leggere un file come flusso di testo, creare l'oggetto scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) e chiamare il metodo [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) per leggere ogni riga del file.</span><span class="sxs-lookup"><span data-stu-id="7485f-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="7485f-119">In modo analogo, si chiama il metodo **Session. enumerate** per ottenere un oggetto [**enumeratore**](enumerator.md) e quindi si chiama il metodo **Enumerator. ReadItem** .</span><span class="sxs-lookup"><span data-stu-id="7485f-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="7485f-120">Come per la lettura dal file di testo, è possibile controllare la proprietà [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) per verificare se è stata raggiunta la fine degli elementi di dati.</span><span class="sxs-lookup"><span data-stu-id="7485f-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="7485f-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="7485f-121">Examples</span></span>

<span data-ttu-id="7485f-122">Nell'esempio VBScript seguente viene chiamato il metodo [**Session. enumerate**](session-enumerate.md) per ottenere un elenco di processi pianificati.</span><span class="sxs-lookup"><span data-stu-id="7485f-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="7485f-123">La subroutine DiplayOutput usa il file di trasformazione XML dello strumento da riga di comando WinRM (WsmTxt. Xsl) per restituire i dati in formato tabulare.</span><span class="sxs-lookup"><span data-stu-id="7485f-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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



## <a name="requirements"></a><span data-ttu-id="7485f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7485f-124">Requirements</span></span>



| <span data-ttu-id="7485f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7485f-125">Requirement</span></span> | <span data-ttu-id="7485f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7485f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7485f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7485f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7485f-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7485f-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="7485f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7485f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7485f-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7485f-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7485f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7485f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7485f-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7485f-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7485f-133">IDL</span><span class="sxs-lookup"><span data-stu-id="7485f-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7485f-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7485f-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7485f-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="7485f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="7485f-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7485f-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7485f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7485f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7485f-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7485f-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7485f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7485f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7485f-140">**Enumeratore**</span><span class="sxs-lookup"><span data-stu-id="7485f-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="7485f-141">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="7485f-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

