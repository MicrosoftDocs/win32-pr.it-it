---
title: Metodo IWMPNetwork setProxySettings
description: Il metodo setProxySettings specifica le impostazioni proxy per un protocollo.
ms.assetid: 6e410812-a06c-4911-8291-1d654fcd281a
keywords:
- Metodo setProxySettings Windows Media Player
- Metodo setProxySettings Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo setProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7fc36c12335cf97ad7bff34924850155f2fd747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333914"
---
# <a name="iwmpnetworksetproxysettings-method"></a><span data-ttu-id="00d6e-106">Metodo IWMPNetwork:: setProxySettings</span><span class="sxs-lookup"><span data-stu-id="00d6e-106">IWMPNetwork::setProxySettings method</span></span>

<span data-ttu-id="00d6e-107">Il metodo **setProxySettings** specifica le impostazioni proxy per un protocollo.</span><span class="sxs-lookup"><span data-stu-id="00d6e-107">The **setProxySettings** method specifies the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d6e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00d6e-108">Syntax</span></span>


```CSharp
public void setProxySettings(
  System.String bstrProtocol,
  System.Int32 lProxySetting
);
```


```VB

Public Sub setProxySettings( _
  ByVal bstrProtocol As System.String, _
  ByVal lProxySetting As System.Int32 _
)
Implements IWMPNetwork.setProxySettings
```





## <a name="parameters"></a><span data-ttu-id="00d6e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="00d6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00d6e-110">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00d6e-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d6e-111">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="00d6e-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="00d6e-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="00d6e-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="00d6e-113">*lProxySetting* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00d6e-113">*lProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00d6e-114">**System. Int32** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="00d6e-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="00d6e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="00d6e-115">Value</span></span> | <span data-ttu-id="00d6e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00d6e-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="00d6e-117">0</span><span class="sxs-lookup"><span data-stu-id="00d6e-117">0</span></span>     | <span data-ttu-id="00d6e-118">Non usare un server proxy.</span><span class="sxs-lookup"><span data-stu-id="00d6e-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="00d6e-119">1</span><span class="sxs-lookup"><span data-stu-id="00d6e-119">1</span></span>     | <span data-ttu-id="00d6e-120">Utilizzare le impostazioni proxy del browser corrente (valido solo per HTTP).</span><span class="sxs-lookup"><span data-stu-id="00d6e-120">Use the proxy settings of the current browser (valid only for HTTP).</span></span> |
| <span data-ttu-id="00d6e-121">2</span><span class="sxs-lookup"><span data-stu-id="00d6e-121">2</span></span>     | <span data-ttu-id="00d6e-122">Usare le impostazioni proxy specificate manualmente.</span><span class="sxs-lookup"><span data-stu-id="00d6e-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="00d6e-123">3</span><span class="sxs-lookup"><span data-stu-id="00d6e-123">3</span></span>     | <span data-ttu-id="00d6e-124">Rilevare automaticamente le impostazioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="00d6e-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00d6e-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00d6e-125">Return value</span></span>

<span data-ttu-id="00d6e-126">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="00d6e-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00d6e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="00d6e-127">Remarks</span></span>

<span data-ttu-id="00d6e-128">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="00d6e-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="00d6e-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="00d6e-129">Examples</span></span>

<span data-ttu-id="00d6e-130">Nell'esempio di codice seguente viene utilizzata una casella di riepilogo per consentire all'utente di impostare l'impostazione del proxy di Windows Media Player per il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="00d6e-130">The following code example uses a list box to allow the user to set the Windows Media Player proxy setting for the HTTP protocol.</span></span> <span data-ttu-id="00d6e-131">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="00d6e-131">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the proxy settings in order so that their index in the
// list box matches their value.
proxySettings.Items.Add("Do not use a proxy server.  (Value = 0)");                                             
proxySettings.Items.Add("Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)");
proxySettings.Items.Add("Use the manually specified proxy settings.  (Value = 2)");
proxySettings.Items.Add("Auto-detect the proxy settings.  (Value = 3)");                                       

// Change the proxy setting for the HTTP protocol when the user makes a list box selection.
private void proxySettings_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the setting from the ListBox
    int setting = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Change the proxy setting. 
    player.network.setProxySettings("HTTP", setting);
}
```


```VB

' Load the list box with the proxy settings in order so that their index in the
&#39; list box matches their value.
proxySettings.Items.Add(&quot;Do not use a proxy server.  (Value = 0)&quot;)
proxySettings.Items.Add(&quot;Use the proxy settings of the current browser. Valid for HTTP only.  (Value = 1)&quot;)
proxySettings.Items.Add(&quot;Use the manually specified proxy settings.  (Value = 2)&quot;)
proxySettings.Items.Add(&quot;Auto-detect the proxy settings.  (Value = 3)&quot;)

&#39; Change the proxy setting for the HTTP protocol when the user makes a list box selection.
Public Sub proxySettings_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles proxySettings.SelectedIndexChanged

    &#39; Store the index of the setting from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim setting As Integer = lb.SelectedIndex

    &#39; Change the proxy setting. 
    player.network.setProxySettings(&quot;HTTP&quot;, setting)
    
End Sub
```





## <a name="requirements"></a><span data-ttu-id="00d6e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00d6e-132">Requirements</span></span>



| <span data-ttu-id="00d6e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d6e-133">Requirement</span></span> | <span data-ttu-id="00d6e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="00d6e-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d6e-135">Versione</span><span class="sxs-lookup"><span data-stu-id="00d6e-135">Version</span></span><br/>   | <span data-ttu-id="00d6e-136">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="00d6e-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="00d6e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="00d6e-137">Namespace</span></span><br/> | <span data-ttu-id="00d6e-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="00d6e-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="00d6e-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="00d6e-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="00d6e-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="00d6e-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d6e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00d6e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d6e-142">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="00d6e-142">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="00d6e-143">**IWMPNetwork. getProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="00d6e-143">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





