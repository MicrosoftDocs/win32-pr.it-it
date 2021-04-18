---
title: IWMPNetwork metodo seproxyname
description: Il metodo seproxyname specifica il nome del server proxy da usare. | IWMPNetwork metodo seproxyname
ms.assetid: a3b0f53a-d81a-4e6d-9cac-7047433246ae
keywords:
- Metodo seproxyname Media Player Windows
- Metodo seproxyname Media Player Windows, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo seproxyname
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9759f37dd4c0e171c09afaea4dfde0993c7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333915"
---
# <a name="iwmpnetworksetproxyname-method"></a><span data-ttu-id="c2f79-107">Metodo IWMPNetwork:: seproxyname</span><span class="sxs-lookup"><span data-stu-id="c2f79-107">IWMPNetwork::setProxyName method</span></span>

<span data-ttu-id="c2f79-108">Il metodo **Seproxyname** specifica il nome del server proxy da usare.</span><span class="sxs-lookup"><span data-stu-id="c2f79-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f79-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2f79-109">Syntax</span></span>


```CSharp
public void setProxyName(
  System.String bstrProtocol,
  System.String bstrProxyName
);
```


```VB

Public Sub setProxyName( _
  ByVal bstrProtocol As System.String, _
  ByVal bstrProxyName As System.String _
)
Implements IWMPNetwork.setProxyName
```





## <a name="parameters"></a><span data-ttu-id="c2f79-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2f79-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2f79-111">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2f79-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f79-112">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="c2f79-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="c2f79-113">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="c2f79-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2f79-114">*bstrProxyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2f79-114">*bstrProxyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f79-115">**System. String** che rappresenta il nome del server proxy da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c2f79-115">A **System.String** that is the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2f79-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2f79-116">Return value</span></span>

<span data-ttu-id="c2f79-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c2f79-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f79-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2f79-118">Remarks</span></span>

<span data-ttu-id="c2f79-119">Questo metodo non ha alcun effetto a meno che il valore recuperato da **IWMPNetwork. getProxySettings** sia 2 (usare le impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="c2f79-119">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="c2f79-120">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="c2f79-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="c2f79-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2f79-121">Examples</span></span>

<span data-ttu-id="c2f79-122">Nell'esempio di codice seguente **viene usato il** nome del proxy per specificare il nome del server proxy di Windows Media Player per il protocollo MMS.</span><span class="sxs-lookup"><span data-stu-id="c2f79-122">The following code example uses **setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="c2f79-123">Il nuovo nome viene recuperato da una casella di testo quando si fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="c2f79-123">The new name is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="c2f79-124">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="c2f79-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setProxyName_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new proxy name.
        string proxyname = nameText.Text;

        // Set the proxy name.
        player.network.setProxyName("MMS", proxyname);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setProxyName_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setProxyName.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new proxy name.
        Dim proxyname As String = nameText.Text

        &#39; Set the proxy name.
        player.network.setProxyName(&quot;MMS&quot;, proxyname)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="c2f79-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2f79-125">Requirements</span></span>



| <span data-ttu-id="c2f79-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f79-126">Requirement</span></span> | <span data-ttu-id="c2f79-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c2f79-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f79-128">Versione</span><span class="sxs-lookup"><span data-stu-id="c2f79-128">Version</span></span><br/>   | <span data-ttu-id="c2f79-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c2f79-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c2f79-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2f79-130">Namespace</span></span><br/> | <span data-ttu-id="c2f79-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c2f79-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c2f79-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="c2f79-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c2f79-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c2f79-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2f79-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2f79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f79-135">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2f79-135">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2f79-136">**IWMPNetwork. getProxyName (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2f79-136">**IWMPNetwork.getProxyName (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyname--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c2f79-137">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="c2f79-137">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





