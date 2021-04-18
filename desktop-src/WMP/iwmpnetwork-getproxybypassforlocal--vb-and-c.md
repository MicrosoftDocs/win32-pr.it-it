---
title: Metodo IWMPNetwork getProxyBypassForLocal
description: Il metodo getProxyBypassForLocal restituisce un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.
ms.assetid: 150a05f3-6979-4a88-a617-472f07d38807
keywords:
- Metodo getProxyBypassForLocal Windows Media Player
- Metodo getProxyBypassForLocal Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo getProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b87b1f00432ec91dd4379a9fa5e31664437afe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327868"
---
# <a name="iwmpnetworkgetproxybypassforlocal-method"></a><span data-ttu-id="936e7-106">Metodo IWMPNetwork:: getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="936e7-106">IWMPNetwork::getProxyBypassForLocal method</span></span>

<span data-ttu-id="936e7-107">Il metodo **getProxyBypassForLocal** restituisce un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="936e7-107">The **getProxyBypassForLocal** method returns a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="936e7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="936e7-108">Syntax</span></span>


```CSharp
public System.Boolean getProxyBypassForLocal(
  System.String bstrProtocol
);
```


```VB

Public Function getProxyBypassForLocal( _
  ByVal bstrProtocol As System.String _
) As System.Boolean
Implements IWMPNetwork.getProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="936e7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="936e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936e7-110">*bstrProtocol*</span><span class="sxs-lookup"><span data-stu-id="936e7-110">*bstrProtocol*</span></span> 
</dt> <dd>

<span data-ttu-id="936e7-111">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="936e7-111">A **System.String** that is the protocol name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="936e7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="936e7-112">Return value</span></span>

<span data-ttu-id="936e7-113">Valore **System. Boolean** che indica se il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="936e7-113">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span> <span data-ttu-id="936e7-114">Il valore è significativo solo quando **IWMPNetwork. getProxySettings** restituisce un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="936e7-114">The value is meaningful only when **IWMPNetwork.getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="936e7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="936e7-115">Remarks</span></span>

<span data-ttu-id="936e7-116">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="936e7-116">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="936e7-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="936e7-117">Examples</span></span>

<span data-ttu-id="936e7-118">Nell'esempio di codice seguente viene usato **getProxyBypassForLocal** per visualizzare se Windows Media Player è impostato in modo da ignorare il server proxy per gli indirizzi locali.</span><span class="sxs-lookup"><span data-stu-id="936e7-118">The following code example uses **getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="936e7-119">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="936e7-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```VB
' Boolean values to hold the results of calls to getProxyBypassForLocal. 
Dim proxyBypassForLocalHTTP As Boolean = False
Dim proxyBypassForLocalMMS As Boolean = False

' Test whether the HTTP proxy settings are manual.
If (player.network.getProxySettings("HTTP") = 2) Then

    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal("HTTP")

End If

' Test whether the MMS proxy settings are manual.
If (player.network.getProxySettings("MMS") = 2) Then

    proxyBypassForLocalMMS = player.network.getProxyBypassForLocal("MMS")

End If

' Store the proxy bypass for local values in a string array and display them
' using a multi-line text box. Unavailable proxy bypass for local values will display
' as "undefined".
proxyInfo(0) = ("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP.ToString())
proxyInfo(1) = ("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS.ToString())
proxyBypassText.Lines = proxyInfo
```


```CSharp

// Boolean values to hold the results of calls to getProxyBypassForLocal. 
bool proxyBypassForLocalHTTP = false;
bool proxyBypassForLocalMMS = false;

// Test whether the HTTP proxy settings are manual.
if (player.network.getProxySettings(&quot;HTTP&quot;) == 2)
{
    proxyBypassForLocalHTTP = player.network.getProxyBypassForLocal(&quot;HTTP&quot;);
}

// Test whether the MMS proxy settings are manual.
if (player.network.getProxySettings(&quot;MMS&quot;) == 2)
{
   proxyBypassForLocalMMS = player.network.getProxyBypassForLocal(&quot;MMS&quot;);
}

// Store the proxy bypass for local values in a string array and display them
// using a multi-line text box. Unavailable proxy bypass for local values will display
// as &quot;undefined&quot;.
proxyInfo[0] = (&quot;The current HTTP proxy bypass for local value: &quot; + proxyBypassForLocalHTTP.ToString());
proxyInfo[1] = (&quot;The current MMS proxy bypass for local value: &quot; + proxyBypassForLocalMMS.ToString());
proxyBypassText.Lines = proxyInfo;
```





## <a name="requirements"></a><span data-ttu-id="936e7-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="936e7-120">Requirements</span></span>



| <span data-ttu-id="936e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="936e7-121">Requirement</span></span> | <span data-ttu-id="936e7-122">Valore</span><span class="sxs-lookup"><span data-stu-id="936e7-122">Value</span></span> |
|----------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="936e7-123">Versione</span><span class="sxs-lookup"><span data-stu-id="936e7-123">Version</span></span><br/>   | <span data-ttu-id="936e7-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="936e7-124">Windows Media Player 9 Series or later</span></span><br/>                                             |
| <span data-ttu-id="936e7-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="936e7-125">Namespace</span></span><br/> | <span data-ttu-id="936e7-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="936e7-126">**WMPLib**</span></span><br/>                                                                         |
| <span data-ttu-id="936e7-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="936e7-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="936e7-128"><dt>Interop.WMPLib.dll</dt></span><span class="sxs-lookup"><span data-stu-id="936e7-128"><dt>Interop.WMPLib.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936e7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="936e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936e7-130">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="936e7-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="936e7-131">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="936e7-131">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="936e7-132">**IWMPNetwork. setProxyBypassForLocal (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="936e7-132">**IWMPNetwork.setProxyBypassForLocal (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxybypassforlocal--vb-and-c.md)
</dt> </dl>

 

 





