---
title: Metodo IWMPNetwork setProxyBypassForLocal
description: Il metodo setProxyBypassForLocal specifica se il server proxy viene ignorato se il server di origine si trova in una rete locale.
ms.assetid: b308957a-0d7e-45be-8625-db198b276dad
keywords:
- Metodo setProxyBypassForLocal Windows Media Player
- Metodo setProxyBypassForLocal Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo setProxyBypassForLocal
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyBypassForLocal
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f869125d43529a039804fe28c0f0dc493f481e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328547"
---
# <a name="iwmpnetworksetproxybypassforlocal-method"></a><span data-ttu-id="18b94-106">Metodo IWMPNetwork:: setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="18b94-106">IWMPNetwork::setProxyBypassForLocal method</span></span>

<span data-ttu-id="18b94-107">Il metodo **setProxyBypassForLocal** specifica se il server proxy viene ignorato se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="18b94-107">The **setProxyBypassForLocal** method specifies whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="18b94-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18b94-108">Syntax</span></span>


```CSharp
public void setProxyBypassForLocal(
  System.String bstrProtocol,
  System.Boolean fBypassForLocal
);
```


```VB

Public Sub setProxyBypassForLocal( _
  ByVal bstrProtocol As System.String, _
  ByVal fBypassForLocal As System.Boolean _
)
Implements IWMPNetwork.setProxyBypassForLocal
```





## <a name="parameters"></a><span data-ttu-id="18b94-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="18b94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18b94-110">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18b94-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b94-111">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="18b94-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="18b94-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="18b94-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="18b94-113">*fBypassForLocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18b94-113">*fBypassForLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18b94-114">Valore **System. Boolean** che indica se il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="18b94-114">A **System.Boolean** value that indicates whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18b94-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18b94-115">Return value</span></span>

<span data-ttu-id="18b94-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="18b94-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18b94-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="18b94-117">Remarks</span></span>

<span data-ttu-id="18b94-118">Questo metodo non ha alcun effetto a meno che il valore recuperato da **IWMPNetwork. getProxySettings** sia 2 (usare le impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="18b94-118">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="18b94-119">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="18b94-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="18b94-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="18b94-120">Examples</span></span>

<span data-ttu-id="18b94-121">Nell'esempio di codice seguente viene usato **setProxyBypassForLocal** per specificare se il server proxy di Windows Media Player viene ignorato, quando si usa il protocollo MMS se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="18b94-121">The following code example uses **setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="18b94-122">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="18b94-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Prepare a message, a caption and buttons for the user prompt.
string message = ("Bypass proxy server for local addresses?");
string caption = "Proxy Settings";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.YesNo;

// Test whether the proxy settings are manual.
if (player.network.getProxySettings("MMS") == 2)
{
    // Prompt the user for a setting. 
    System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

    // Store the return value of the DialogResult in a boolean variable.
    bool proxybypass;
    
    if(result == System.Windows.Forms.DialogResult.Yes)
    {
        proxybypass = true;
    }
    else
    {
        proxybypass = false;
    }

    // Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal("MMS", proxybypass);
}
else
{
    // Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
}
```


```VB

' Prepare a message, a caption and buttons for the user prompt.
Dim message As String = &quot;Bypass proxy server for local addresses?&quot;
Dim caption As String = &quot;Proxy Settings&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.YesNo

&#39; Test whether the proxy settings are manual.
If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

    &#39; Prompt the user for a setting. 
    Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

    &#39; Store the return value of the DialogResult as a boolean.
    Dim proxybypass As Boolean

    If (result = System.Windows.Forms.DialogResult.Yes) Then

        proxybypass = True

    Else

        proxybypass = False

    End If

    &#39; Set the proxy bypass value according to the response.
    player.network.setProxyBypassForLocal(&quot;MMS&quot;, proxybypass)

Else

    &#39; Warn that proxy settings must be set to 2 (manual).
    System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="18b94-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18b94-123">Requirements</span></span>



| <span data-ttu-id="18b94-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="18b94-124">Requirement</span></span> | <span data-ttu-id="18b94-125">Valore</span><span class="sxs-lookup"><span data-stu-id="18b94-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18b94-126">Versione</span><span class="sxs-lookup"><span data-stu-id="18b94-126">Version</span></span><br/>   | <span data-ttu-id="18b94-127">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="18b94-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="18b94-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="18b94-128">Namespace</span></span><br/> | <span data-ttu-id="18b94-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="18b94-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="18b94-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="18b94-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="18b94-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="18b94-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18b94-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18b94-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18b94-133">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18b94-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18b94-134">**IWMPNetwork. getProxyBypassForLocal (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18b94-134">**IWMPNetwork.getProxyBypassForLocal (VB and C#)**</span></span>](iwmpnetwork-getproxybypassforlocal--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="18b94-135">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="18b94-135">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





