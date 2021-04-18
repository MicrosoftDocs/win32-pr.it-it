---
title: Metodo getProxyName IWMPNetwork
description: Il metodo getProxyName restituisce il nome del server proxy in uso.
ms.assetid: 69396b01-1da7-450c-b229-0cc4fb832ae9
keywords:
- Metodo getProxyName Media Player Windows
- Metodo getProxyName Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo getProxyName
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5e05b6552e5e6a922cf02037a0bfc4956bfc28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324716"
---
# <a name="iwmpnetworkgetproxyname-method"></a><span data-ttu-id="dc1fe-106">Metodo IWMPNetwork:: getProxyName</span><span class="sxs-lookup"><span data-stu-id="dc1fe-106">IWMPNetwork::getProxyName method</span></span>

<span data-ttu-id="dc1fe-107">Il metodo **getProxyName** restituisce il nome del server proxy in uso.</span><span class="sxs-lookup"><span data-stu-id="dc1fe-107">The **getProxyName** method returns the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc1fe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc1fe-108">Syntax</span></span>


```CSharp
public System.String getProxyName(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyName( _
  ByVal bstrProtocol As System.String _
) As System.String
Implements IWMPNetwork.getProxyName
```





## <a name="parameters"></a><span data-ttu-id="dc1fe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc1fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc1fe-110">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc1fe-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc1fe-111">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="dc1fe-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="dc1fe-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="dc1fe-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc1fe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc1fe-113">Return value</span></span>

<span data-ttu-id="dc1fe-114">**System. String** che rappresenta il nome del server proxy in uso.</span><span class="sxs-lookup"><span data-stu-id="dc1fe-114">A **System.String** that is the name of the proxy server being used.</span></span> <span data-ttu-id="dc1fe-115">Il valore è significativo solo quando **IWMPNetwork. getProxySettings** restituisce un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="dc1fe-115">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc1fe-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc1fe-116">Remarks</span></span>

<span data-ttu-id="dc1fe-117">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="dc1fe-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="dc1fe-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc1fe-118">Examples</span></span>

<span data-ttu-id="dc1fe-119">Nell'esempio di codice seguente viene usato **getProxyName** per visualizzare i nomi dei server proxy di Windows Media Player per i protocolli http e MMS.</span><span class="sxs-lookup"><span data-stu-id="dc1fe-119">The following code example uses **getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="dc1fe-120">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="dc1fe-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// String values to hold the results of calls to getProxyExceptionList. 
string proxyNameHTTP = "";
string proxyNameMMS = "";

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings("HTTP") == 2)
{
    proxyNameHTTP = player.network.getProxyName("HTTP");
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    proxyNameMMS = player.network.getProxyName("MMS");
}

// Store the proxy server names in a string array and display them using a multi-line
// text box. Unavailable proxy server names will display as "undefined".
proxyNames[0] = ("The current HTTP proxy server name is: " + proxyNameHTTP);
proxyNames[1] = ("The current MMS proxy server name is: " + proxyNameMMS);
proxyNameText.Lines = proxyNames;
```


```VB

' String values to hold the results of calls to getProxyExceptionList. 
Dim proxyNameHTTP As String = &quot;&quot;
Dim proxyNameMMS As String = &quot;&quot;

&#39; Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings(&quot;HTTP&quot;) = 2) Then

    proxyNameHTTP = player.network.getProxyName(&quot;HTTP&quot;)

End If

&#39; Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    proxyNameMMS = player.network.getProxyName(&quot;MMS&quot;)

End If

&#39; Store the proxy server names in a string array and display them using a multi-line
&#39; text box. Unavailable proxy server names will display as &quot;undefined&quot;.
proxyNames(0) = (&quot;The current HTTP proxy server name is: &quot; + proxyNameHTTP)
proxyNames(1) = (&quot;The current MMS proxy server name is: &quot; + proxyNameMMS)
proxyNameText.Lines = proxyNames
```





## <a name="requirements"></a><span data-ttu-id="dc1fe-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc1fe-121">Requirements</span></span>



| <span data-ttu-id="dc1fe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc1fe-122">Requirement</span></span> | <span data-ttu-id="dc1fe-123">Valore</span><span class="sxs-lookup"><span data-stu-id="dc1fe-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc1fe-124">Versione</span><span class="sxs-lookup"><span data-stu-id="dc1fe-124">Version</span></span><br/>   | <span data-ttu-id="dc1fe-125">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="dc1fe-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dc1fe-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc1fe-126">Namespace</span></span><br/> | <span data-ttu-id="dc1fe-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dc1fe-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dc1fe-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="dc1fe-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dc1fe-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dc1fe-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc1fe-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc1fe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc1fe-131">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc1fe-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc1fe-132">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc1fe-132">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dc1fe-133">**IWMPNetwork. seproxyname (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="dc1fe-133">**IWMPNetwork.setProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxyname--vb-and-c.md)
</dt> </dl>

 

 





