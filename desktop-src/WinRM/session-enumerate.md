---
title: Metodo Session. enumerate (WSManDisp. h)
description: Enumera una tabella, una raccolta dati o una risorsa di log.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumera il metodo Gestione remota Windows
- Enumerazione Gestione remota Windows metodo, oggetto Session
- Gestione remota Windows oggetto sessione, metodo enumerate
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048135"
---
# <a name="sessionenumerate-method"></a><span data-ttu-id="136e8-106">Metodo Session. enumerate</span><span class="sxs-lookup"><span data-stu-id="136e8-106">Session.Enumerate method</span></span>

<span data-ttu-id="136e8-107">Enumera una tabella, una raccolta dati o una risorsa di log.</span><span class="sxs-lookup"><span data-stu-id="136e8-107">Enumerates a table, data collection, or log resource.</span></span> <span data-ttu-id="136e8-108">Per creare una query, includere un parametro di *filtro* e un parametro *dialetto* in un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="136e8-108">To create a query, include a *filter* parameter and a *dialect* parameter in an enumeration.</span></span> <span data-ttu-id="136e8-109">È anche possibile usare un oggetto [**resourceLocator**](resourcelocator.md) per creare query.</span><span class="sxs-lookup"><span data-stu-id="136e8-109">You can also use a [**ResourceLocator**](resourcelocator.md) object to create queries.</span></span> <span data-ttu-id="136e8-110">Per ulteriori informazioni, vedere [enumerazione o visualizzazione di un elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="136e8-110">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="136e8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="136e8-111">Syntax</span></span>


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="136e8-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="136e8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="136e8-113">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="136e8-113">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="136e8-114">Identificatore della risorsa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="136e8-114">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="136e8-115">Questo parametro può contenere uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="136e8-115">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="136e8-116">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="136e8-116">The URI of the resource.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   <span data-ttu-id="136e8-117">Oggetto [**resourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="136e8-117">A [**ResourceLocator**](resourcelocator.md) object.</span></span>
-   <span data-ttu-id="136e8-118">Riferimento all'endpoint di [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="136e8-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="136e8-119">Per ulteriori informazioni sulla specifica pubblica per [protocollo WS-Management](ws-management-protocol.md), vedere la [pagina](/previous-versions/dotnet/articles/ms951267(v=msdn.10))relativa all'indice delle specifiche di gestione.</span><span class="sxs-lookup"><span data-stu-id="136e8-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="136e8-120">*filtro* \[ di in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="136e8-120">*filter* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="136e8-121">Filtro che definisce quali elementi della risorsa vengono restituiti dall'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="136e8-121">A filter that defines what items in the resource are returned by the enumeration.</span></span> <span data-ttu-id="136e8-122">Quando la risorsa viene enumerata, vengono restituiti solo gli elementi che corrispondono ai criteri di filtro.</span><span class="sxs-lookup"><span data-stu-id="136e8-122">When the resource is enumerated, only those items that match the filter criteria are returned.</span></span> <span data-ttu-id="136e8-123">L'inclusione di un parametro di *filtro* e di un parametro *dialetto* in un'enumerazione converte l'enumerazione in una query.</span><span class="sxs-lookup"><span data-stu-id="136e8-123">Including a *filter* parameter and a *dialect* parameter in an enumeration converts the enumeration into a query.</span></span> <span data-ttu-id="136e8-124">Per un esempio, vedere [esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="136e8-124">For an example, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

<span data-ttu-id="136e8-125">Se si dispone di un oggetto [**resourceLocator**](resourcelocator.md) per il parametro *resourceUri* , questo parametro non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="136e8-125">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="136e8-126">*dialetto* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="136e8-126">*dialect* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="136e8-127">Lingua utilizzata dal filtro.</span><span class="sxs-lookup"><span data-stu-id="136e8-127">The language used by the filter.</span></span> <span data-ttu-id="136e8-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), un subset di SQL utilizzato da WMI, è l'unico linguaggio supportato.</span><span class="sxs-lookup"><span data-stu-id="136e8-128">[WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), a subset of SQL used by WMI, is the only language supported.</span></span>

<span data-ttu-id="136e8-129">Se si dispone di un oggetto [**resourceLocator**](resourcelocator.md) per il parametro *resourceUri* , questo parametro non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="136e8-129">If you have a [**ResourceLocator**](resourcelocator.md) object for the *resourceURI* parameter, then this parameter should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="136e8-130">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="136e8-130">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="136e8-131">Parametro che deve contenere un flag nell'enumerazione **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="136e8-131">A parameter that must contain a flag in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="136e8-132">Per altre informazioni, vedere [costanti di enumerazione](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="136e8-132">For more information, see [Enumeration Constants](enumeration-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="136e8-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="136e8-133">Return value</span></span>

<span data-ttu-id="136e8-134">Oggetto [**enumeratore**](enumerator.md) che contiene i risultati dell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="136e8-134">An [**Enumerator**](enumerator.md) object that contains the results of the enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="136e8-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="136e8-135">Remarks</span></span>

<span data-ttu-id="136e8-136">Per ulteriori informazioni sulla limitazione delle chiamate di rete durante un'enumerazione, vedere la proprietà [**BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="136e8-136">For more information about limiting network calls during an enumeration, see the [**BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="136e8-137">Tenere presente che se i flag includono le [**costanti di enumerazione**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** o **WSManFlagHierarchyShallow** , gestione remota Windows servizio restituisce il codice di errore **errore \_ WSMan modalità di \_ polimorfismo non \_ \_ supportata**.</span><span class="sxs-lookup"><span data-stu-id="136e8-137">Be aware that if the flags include the [**Enumeration Constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** or **WSManFlagHierarchyShallow** then Windows Remote Management service returns the error code **ERROR\_WSMAN\_POLYMORPHISM\_MODE\_UNSUPPORTED**.</span></span>

<span data-ttu-id="136e8-138">Se viene specificato un filtro, è necessario che sia un documento valido rispetto allo schema della risorsa.</span><span class="sxs-lookup"><span data-stu-id="136e8-138">If a filter is specified, it must be a valid document with respect to the schema of the resource.</span></span> <span data-ttu-id="136e8-139">Il parametro Dialect è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="136e8-139">The dialect parameter is optional.</span></span> <span data-ttu-id="136e8-140">Tuttavia, se la stringa di filtro inizia con <, ma non è un frammento XML, includere il parametro *dialect* o impostare il flag **WSManFlagNonXmlText** nel parametro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="136e8-140">However, if the filter string begins with <, but is not an XML fragment, then either include the *dialect* parameter or set the **WSManFlagNonXmlText** flag in the *flags* parameter.</span></span> <span data-ttu-id="136e8-141">Per altre informazioni, vedere [**costanti di enumerazione**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="136e8-141">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

<span data-ttu-id="136e8-142">Il metodo C++ corrispondente è [**IWSManSession:: enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="136e8-142">The corresponding C++ method is [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

## <a name="examples"></a><span data-ttu-id="136e8-143">Esempio</span><span class="sxs-lookup"><span data-stu-id="136e8-143">Examples</span></span>

<span data-ttu-id="136e8-144">Nell'esempio di codice VBScript riportato di seguito vengono enumerate le istanze [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in un computer remoto specificato dal nome di dominio completo (servername.Domain.com).</span><span class="sxs-lookup"><span data-stu-id="136e8-144">The following VBScript code example enumerates the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instances on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="136e8-145">Tenere presente che liberare l'oggetto di enumerazione Cancella le richieste di enumerazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="136e8-145">Be aware that freeing the enumeration object clears pending enumeration requests.</span></span> <span data-ttu-id="136e8-146">La subroutine DiplayOutput usa il file di trasformazione XML dello strumento da riga di comando WinRM (WsmTxt. Xsl) per restituire i dati in formato tabulare.</span><span class="sxs-lookup"><span data-stu-id="136e8-146">The DisplayOutput subroutine uses the Winrm command-line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

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



## <a name="requirements"></a><span data-ttu-id="136e8-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="136e8-147">Requirements</span></span>



| <span data-ttu-id="136e8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="136e8-148">Requirement</span></span> | <span data-ttu-id="136e8-149">Valore</span><span class="sxs-lookup"><span data-stu-id="136e8-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="136e8-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="136e8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="136e8-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="136e8-151">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="136e8-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="136e8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="136e8-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="136e8-153">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="136e8-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="136e8-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="136e8-155"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="136e8-155"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="136e8-156">IDL</span><span class="sxs-lookup"><span data-stu-id="136e8-156">IDL</span></span><br/>                      | <dl> <span data-ttu-id="136e8-157"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="136e8-157"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="136e8-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="136e8-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="136e8-159"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="136e8-159"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="136e8-160">DLL</span><span class="sxs-lookup"><span data-stu-id="136e8-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="136e8-161"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="136e8-161"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="136e8-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="136e8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136e8-163">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="136e8-163">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="136e8-164">Esecuzione di query per istanze specifiche di una risorsa</span><span class="sxs-lookup"><span data-stu-id="136e8-164">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="136e8-165">**BatchItems**</span><span class="sxs-lookup"><span data-stu-id="136e8-165">**BatchItems**</span></span>](session-batchitems.md)
</dt> <dt>

[<span data-ttu-id="136e8-166">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="136e8-166">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

