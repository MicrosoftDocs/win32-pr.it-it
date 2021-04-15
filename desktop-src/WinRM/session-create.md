---
title: Metodo Session. Create (WSManDisp. h)
description: Crea una nuova istanza di una risorsa e restituisce il riferimento all'endpoint (EPR) del nuovo oggetto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows crea metodo
- Crea Gestione remota Windows metodo, oggetto sessione
- Gestione remota Windows oggetto sessione, metodo create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477686"
---
# <a name="sessioncreate-method"></a><span data-ttu-id="8937d-106">Metodo Session. Create</span><span class="sxs-lookup"><span data-stu-id="8937d-106">Session.Create method</span></span>

<span data-ttu-id="8937d-107">Crea una nuova istanza di una risorsa e restituisce il [*riferimento all'endpoint (EPR)*](windows-remote-management-glossary.md) del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8937d-107">Creates a new instance of a resource and returns the [*endpoint reference (EPR)*](windows-remote-management-glossary.md) of the new object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8937d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8937d-108">Syntax</span></span>


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8937d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8937d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8937d-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8937d-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8937d-111">Identificatore della risorsa da creare.</span><span class="sxs-lookup"><span data-stu-id="8937d-111">Identifier of the resource to create.</span></span>

<span data-ttu-id="8937d-112">Questo parametro può contenere uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="8937d-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="8937d-113">URI con uno o più [*selettori*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="8937d-113">URI with one or more [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="8937d-114">Tenere presente che il [*plug-in WMI*](windows-remote-management-glossary.md) non supporta la creazione di risorse diverse da un listener di [protocollo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="8937d-114">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a [WS-Management Protocol](ws-management-protocol.md) listener.</span></span>
-   <span data-ttu-id="8937d-115">Oggetto [**resourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*Opzioni*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="8937d-115">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="8937d-116">Riferimento a endpoint [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="8937d-116">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="8937d-117">Per ulteriori informazioni sulla specifica pubblica per il protocollo WS-Management, vedere la pagina relativa all' [Indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="8937d-117">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="8937d-118">*risorse*</span><span class="sxs-lookup"><span data-stu-id="8937d-118">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="8937d-119">XML che contiene il contenuto della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8937d-119">The XML that contains resource content.</span></span>

</dd> <dt>

<span data-ttu-id="8937d-120">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="8937d-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8937d-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="8937d-121">Reserved.</span></span> <span data-ttu-id="8937d-122">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="8937d-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8937d-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8937d-123">Return value</span></span>

<span data-ttu-id="8937d-124">EPR della nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="8937d-124">The EPR of the new resource.</span></span>

## <a name="remarks"></a><span data-ttu-id="8937d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8937d-125">Remarks</span></span>

<span data-ttu-id="8937d-126">**Session. Create** viene usato solo per la creazione di nuove istanze di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8937d-126">**Session.Create** is only used for creating new instances of a resource.</span></span> <span data-ttu-id="8937d-127">Usare il metodo [**Session. Put**](session-put.md) per aggiornare le istanze esistenti di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="8937d-127">Use the [**Session.Put**](session-put.md) method to update existing instances of a resource.</span></span> <span data-ttu-id="8937d-128">Dopo aver ottenuto il nuovo URI della risorsa, è possibile chiamare [**Session. Get**](session-get.md) per recuperare il nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8937d-128">After you obtain the new resource URI, you can call [**Session.Get**](session-get.md) to retrieve the new object.</span></span> <span data-ttu-id="8937d-129">Il nuovo oggetto contiene tutte le proprietà assegnate dal provider di risorse durante la creazione del nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8937d-129">The new object contains any properties that the resource provider assigns when creating the new object.</span></span> <span data-ttu-id="8937d-130">Se, ad esempio, si crea un nuovo [*listener*](windows-remote-management-glossary.md) del protocollo WS-Management e si recupera l'oggetto listener utilizzando **Session. Get**, sarà possibile ottenere anche le proprietà **Port**, **Enabled** e **ListeningOn** .</span><span class="sxs-lookup"><span data-stu-id="8937d-130">For example, if you create a new WS-Management protocol [*listener*](windows-remote-management-glossary.md) and retrieve the listener object using **Session.Get**, then you also obtain the **Port**, **Enabled**, and **ListeningOn** properties.</span></span>

<span data-ttu-id="8937d-131">Tenere presente che il [*plug-in WMI*](windows-remote-management-glossary.md) non supporta la creazione di risorse diverse da un listener del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="8937d-131">Be aware that the [*WMI plug-in*](windows-remote-management-glossary.md) does not support creating any resource other than a WS-Management protocol listener.</span></span>

<span data-ttu-id="8937d-132">Per chiamare questo metodo, viene usata la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="8937d-132">The following syntax is used to call this method.</span></span>


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a><span data-ttu-id="8937d-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="8937d-133">Examples</span></span>

<span data-ttu-id="8937d-134">Nell'esempio di codice VBScript seguente viene chiamato **Session. Create** per creare un listener nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="8937d-134">The following VBScript code example calls **Session.Create** to create a listener on the local computer.</span></span>


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
```



## <a name="requirements"></a><span data-ttu-id="8937d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8937d-135">Requirements</span></span>



| <span data-ttu-id="8937d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8937d-136">Requirement</span></span> | <span data-ttu-id="8937d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="8937d-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8937d-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8937d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8937d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8937d-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8937d-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8937d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8937d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8937d-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8937d-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8937d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8937d-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8937d-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8937d-144">IDL</span><span class="sxs-lookup"><span data-stu-id="8937d-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8937d-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8937d-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="8937d-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="8937d-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="8937d-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8937d-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8937d-148">DLL</span><span class="sxs-lookup"><span data-stu-id="8937d-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8937d-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8937d-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8937d-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8937d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8937d-151">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="8937d-151">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="8937d-152">Protocollo WS-Management</span><span class="sxs-lookup"><span data-stu-id="8937d-152">WS-Management Protocol</span></span>](ws-management-protocol.md)
</dt> </dl>

 

