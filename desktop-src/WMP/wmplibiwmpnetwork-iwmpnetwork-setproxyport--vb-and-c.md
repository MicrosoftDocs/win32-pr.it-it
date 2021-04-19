---
title: Metodo IWMPNetwork setProxyPort
description: Il metodo setProxyPort specifica la porta proxy da usare. | Metodo IWMPNetwork setProxyPort
ms.assetid: df4b33f6-52b5-437f-ade2-0d08ca2878a9
keywords:
- Metodo setProxyPort Windows Media Player
- Metodo setProxyPort Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo setProxyPort
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyPort
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d171fa1afc129dd1d13c1d9d12d71c4370cba9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331733"
---
# <a name="iwmpnetworksetproxyport-method"></a><span data-ttu-id="3c60e-107">Metodo IWMPNetwork:: setProxyPort</span><span class="sxs-lookup"><span data-stu-id="3c60e-107">IWMPNetwork::setProxyPort method</span></span>

<span data-ttu-id="3c60e-108">Il metodo **setProxyPort** specifica la porta proxy da usare.</span><span class="sxs-lookup"><span data-stu-id="3c60e-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c60e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c60e-109">Syntax</span></span>


```CSharp
public void setProxyPort(
  System.String bstrProtocol,
  System.Int32 lProxyPort
);
```


```VB

Public Sub setProxyPort( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxyPort As System.Int32 _
)
Implements IWMPNetwork.setProxyPort
```





## <a name="parameters"></a><span data-ttu-id="3c60e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c60e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c60e-111">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c60e-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c60e-112">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="3c60e-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="3c60e-113">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="3c60e-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c60e-114">*lProxyPort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c60e-114">*lProxyPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c60e-115">**System. Int32** che rappresenta la porta proxy da usare.</span><span class="sxs-lookup"><span data-stu-id="3c60e-115">A **System.Int32** that is the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c60e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c60e-116">Return value</span></span>

<span data-ttu-id="3c60e-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3c60e-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c60e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c60e-118">Remarks</span></span>

<span data-ttu-id="3c60e-119">Questo metodo non ha alcun effetto a meno che il valore recuperato da **IWMPNetwork. getProxySettings** sia 2 (usare le impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="3c60e-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="3c60e-120">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="3c60e-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="3c60e-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="3c60e-121">Examples</span></span>

<span data-ttu-id="3c60e-122">Nell'esempio di codice seguente viene usato **setProxyPort** per specificare il numero di porta del proxy di Windows Media Player per il protocollo MMS.</span><span class="sxs-lookup"><span data-stu-id="3c60e-122">The following code example uses **setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="3c60e-123">Il numero di porta viene recuperato da una casella di testo quando si fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="3c60e-123">The port number is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="3c60e-124">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="3c60e-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyPort_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy port number.
        int portnumber = System.Convert.ToInt32(portText.Text);

        // Set the proxy port.
        player.network.setProxyPort("MMS", portnumber);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyPort_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyPort.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy port number.
        Dim portnumber As Integer = System.Convert.ToInt32(portText.Text)

        &#39; Set the proxy port.
        player.network.setProxyPort(&quot;MMS&quot;, portnumber)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3c60e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c60e-125">Requirements</span></span>



| <span data-ttu-id="3c60e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c60e-126">Requirement</span></span> | <span data-ttu-id="3c60e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3c60e-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c60e-128">Versione</span><span class="sxs-lookup"><span data-stu-id="3c60e-128">Version</span></span><br/>   | <span data-ttu-id="3c60e-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3c60e-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3c60e-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3c60e-130">Namespace</span></span><br/> | <span data-ttu-id="3c60e-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3c60e-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3c60e-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="3c60e-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3c60e-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3c60e-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c60e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c60e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c60e-135">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3c60e-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c60e-136">**IWMPNetwork. getProxyPort (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3c60e-136">**IWMPNetwork.getProxyPort (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyport--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c60e-137">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="3c60e-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





