---
title: Metodo IWMPNetwork setProxyExceptionList
description: Il metodo setProxyExceptionList specifica l'elenco di eccezioni del proxy. | Metodo IWMPNetwork setProxyExceptionList
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- Metodo setProxyExceptionList Windows Media Player
- Metodo setProxyExceptionList Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo setProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333917"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="1075a-107">Metodo IWMPNetwork:: setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="1075a-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="1075a-108">Il metodo **setProxyExceptionList** specifica l'elenco di eccezioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="1075a-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1075a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1075a-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="1075a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1075a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1075a-111">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1075a-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1075a-112">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="1075a-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="1075a-113">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1075a-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1075a-114">*pbstrExceptionList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1075a-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1075a-115">**System. String** che rappresenta un elenco delimitato da punti e virgola di host per i quali il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1075a-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="1075a-116">Gli spazi iniziali e finali non devono essere presenti.</span><span class="sxs-lookup"><span data-stu-id="1075a-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1075a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1075a-117">Return value</span></span>

<span data-ttu-id="1075a-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1075a-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1075a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1075a-119">Remarks</span></span>

<span data-ttu-id="1075a-120">Si tratta di un elenco di computer, domini e/o indirizzi che ignoreranno il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="1075a-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="1075a-121">Il \* carattere può essere usato come carattere jolly per elencare le voci.</span><span class="sxs-lookup"><span data-stu-id="1075a-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="1075a-122">Ad esempio, \* . com corrisponde a tutti gli host nel dominio com, mentre 67. \* corrisponderebbe a tutti gli host della classe 67 una subnet.</span><span class="sxs-lookup"><span data-stu-id="1075a-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="1075a-123">Questo metodo non ha alcun effetto a meno che il valore recuperato da **IWMPNetwork. getProxySettings** sia 2 (usare le impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="1075a-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="1075a-124">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="1075a-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="1075a-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="1075a-125">Examples</span></span>

<span data-ttu-id="1075a-126">Nell'esempio di codice seguente viene usato **setProxyExceptionList** per specificare un elenco di host per cui il server proxy viene ignorato quando si usa il protocollo MMS.</span><span class="sxs-lookup"><span data-stu-id="1075a-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="1075a-127">Il nuovo elenco viene recuperato da una casella di testo quando si fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="1075a-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="1075a-128">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="1075a-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1075a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1075a-129">Requirements</span></span>



| <span data-ttu-id="1075a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1075a-130">Requirement</span></span> | <span data-ttu-id="1075a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1075a-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1075a-132">Versione</span><span class="sxs-lookup"><span data-stu-id="1075a-132">Version</span></span><br/>   | <span data-ttu-id="1075a-133">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1075a-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1075a-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1075a-134">Namespace</span></span><br/> | <span data-ttu-id="1075a-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1075a-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1075a-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="1075a-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1075a-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1075a-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1075a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1075a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1075a-139">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1075a-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1075a-140">**IWMPNetwork. getProxyExceptionList (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1075a-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1075a-141">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="1075a-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





