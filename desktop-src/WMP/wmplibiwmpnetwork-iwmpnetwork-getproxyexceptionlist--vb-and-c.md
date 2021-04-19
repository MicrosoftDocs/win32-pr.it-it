---
title: Metodo IWMPNetwork getProxyExceptionList
description: Il metodo getProxyExceptionList restituisce l'elenco di eccezioni del proxy.
ms.assetid: 1b209d75-0fa7-420e-831c-160f3826cf3a
keywords:
- Metodo getProxyExceptionList Windows Media Player
- Metodo getProxyExceptionList Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo getProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402e3b28d5423314b499213c9ddb02bca482d629
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324717"
---
# <a name="iwmpnetworkgetproxyexceptionlist-method"></a><span data-ttu-id="03594-106">Metodo IWMPNetwork:: getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="03594-106">IWMPNetwork::getProxyExceptionList method</span></span>

<span data-ttu-id="03594-107">Il metodo **getProxyExceptionList** restituisce l'elenco di eccezioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="03594-107">The **getProxyExceptionList** method returns the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="03594-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03594-108">Syntax</span></span>


```CSharp
public System.String getProxyExceptionList(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyExceptionList( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="03594-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="03594-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03594-110">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03594-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03594-111">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="03594-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="03594-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="03594-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03594-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03594-113">Return value</span></span>

<span data-ttu-id="03594-114">**System. String** che rappresenta un elenco delimitato da punti e virgola di host per i quali il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="03594-114">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="03594-115">Il valore è significativo solo quando **IWMPNetwork. getProxySettings** restituisce un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="03594-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="03594-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="03594-116">Remarks</span></span>

<span data-ttu-id="03594-117">Si tratta di un elenco di computer, domini e/o indirizzi che ignoreranno il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="03594-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="03594-118">Il \* carattere può essere usato come carattere jolly per elencare le voci.</span><span class="sxs-lookup"><span data-stu-id="03594-118">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="03594-119">Ad esempio, \* . com corrisponde a tutti gli host nel dominio com, mentre 67. \* corrisponderebbe a tutti gli host della classe 67 una subnet.</span><span class="sxs-lookup"><span data-stu-id="03594-119">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="03594-120">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="03594-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="03594-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="03594-121">Examples</span></span>

<span data-ttu-id="03594-122">Nell'esempio di codice seguente viene usato **getProxyExceptionList** per visualizzare se Windows Media Player è impostato in modo da ignorare il server proxy per gli indirizzi locali.</span><span class="sxs-lookup"><span data-stu-id="03594-122">The following code example uses **getProxyExceptionList** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="03594-123">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="03594-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyExceptionListHTTP = "";
string proxyExceptionListMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyExceptionListHTTP = player.network.getProxyExceptionList("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyExceptionListMMS = player.network.getProxyExceptionList("MMS");
}

// Store the proxy exception lists in a string array and display them
// using a multi-line text box. Unavailable exception lists will display
// as "undefined".
proxyExList[0] = ("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
proxyExList[1] = ("The current MMS proxy exception list: " + proxyExceptionListMMS);
proxyExceptionListText.Lines = proxyExList;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyExceptionListHTTP As String = &quot;&quot;
Dim proxyExceptionListMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyExceptionListHTTP = player.network.getProxyExceptionList(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyExceptionListMMS = player.network.getProxyExceptionList(&quot;MMS&quot;)

End If

&#39; Store the proxy exception lists in a string array and display them
&#39; using a multi-line text box. Unavailable exception lists will display
&#39; as &quot;undefined&quot;.
proxyExList(0) = (&quot;The current HTTP proxy exception list: &quot; + proxyExceptionListHTTP)
proxyExList(1) = (&quot;The current MMS proxy exception list: &quot; + proxyExceptionListMMS)
proxyExceptionList.Lines = proxyExList
```





## <a name="requirements"></a><span data-ttu-id="03594-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03594-124">Requirements</span></span>



| <span data-ttu-id="03594-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="03594-125">Requirement</span></span> | <span data-ttu-id="03594-126">Valore</span><span class="sxs-lookup"><span data-stu-id="03594-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03594-127">Versione</span><span class="sxs-lookup"><span data-stu-id="03594-127">Version</span></span><br/>   | <span data-ttu-id="03594-128">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="03594-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="03594-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03594-129">Namespace</span></span><br/> | <span data-ttu-id="03594-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="03594-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="03594-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="03594-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="03594-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="03594-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03594-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03594-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03594-134">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="03594-134">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03594-135">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="03594-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03594-136">**IWMPNetwork. setProxyExceptionList (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="03594-136">**IWMPNetwork.setProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyexceptionlist--vb-and-c.md)
</dt> </dl>

 

 





