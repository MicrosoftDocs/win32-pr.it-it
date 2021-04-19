---
title: Metodo IWMPNetwork getProxySettings
description: Il metodo getProxySettings restituisce informazioni sulle impostazioni proxy per un protocollo.
ms.assetid: eda4829a-4869-4557-8fe9-8061a1e0f586
keywords:
- Metodo getProxySettings Windows Media Player
- Metodo getProxySettings Windows Media Player, interfaccia IWMPNetwork
- Interfaccia IWMPNetwork Windows Media Player, metodo getProxySettings
topic_type:
- apiref
api_name:
- IWMPNetwork.getProxySettings
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d970160c07c90e84585c87ed1abf740fbe3c6318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329913"
---
# <a name="iwmpnetworkgetproxysettings-method"></a><span data-ttu-id="46772-106">Metodo IWMPNetwork:: getProxySettings</span><span class="sxs-lookup"><span data-stu-id="46772-106">IWMPNetwork::getProxySettings method</span></span>

<span data-ttu-id="46772-107">Il metodo **getProxySettings** restituisce informazioni sulle impostazioni proxy per un protocollo.</span><span class="sxs-lookup"><span data-stu-id="46772-107">The **getProxySettings** method returns information about the proxy settings for a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="46772-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46772-108">Syntax</span></span>


```CSharp
public System.Int32 getProxySettings(
  System.String bstrProtocol
);
```


```VB

Public Function getProxySettings( _
  ByVal bstrProtocol As System.String _
) As System.Int32
Implements IWMPNetwork.getProxySettings
```





## <a name="parameters"></a><span data-ttu-id="46772-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="46772-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46772-110">*bstrProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46772-110">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46772-111">**System. String** che rappresenta il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="46772-111">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="46772-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="46772-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46772-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46772-113">Return value</span></span>

<span data-ttu-id="46772-114">**System. Int32** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="46772-114">A **System.Int32** that is one of the following values.</span></span>



| <span data-ttu-id="46772-115">Valore</span><span class="sxs-lookup"><span data-stu-id="46772-115">Value</span></span> | <span data-ttu-id="46772-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46772-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="46772-117">0</span><span class="sxs-lookup"><span data-stu-id="46772-117">0</span></span>     | <span data-ttu-id="46772-118">Non è in uso un server proxy.</span><span class="sxs-lookup"><span data-stu-id="46772-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="46772-119">1</span><span class="sxs-lookup"><span data-stu-id="46772-119">1</span></span>     | <span data-ttu-id="46772-120">Vengono usate le impostazioni proxy per il browser corrente (valido solo per HTTP).</span><span class="sxs-lookup"><span data-stu-id="46772-120">The proxy settings for the current browser are being used (valid only for HTTP).</span></span> |
| <span data-ttu-id="46772-121">2</span><span class="sxs-lookup"><span data-stu-id="46772-121">2</span></span>     | <span data-ttu-id="46772-122">Sono in uso le impostazioni proxy specificate manualmente.</span><span class="sxs-lookup"><span data-stu-id="46772-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="46772-123">3</span><span class="sxs-lookup"><span data-stu-id="46772-123">3</span></span>     | <span data-ttu-id="46772-124">Le impostazioni proxy vengono rilevate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="46772-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="46772-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="46772-125">Remarks</span></span>

<span data-ttu-id="46772-126">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="46772-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="46772-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="46772-127">Examples</span></span>

<span data-ttu-id="46772-128">Nell'esempio di codice seguente viene usato **getProxySettings** per visualizzare un messaggio, che fornisce informazioni sulle impostazioni proxy correnti del lettore, in un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="46772-128">The following code example uses **getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in a label.</span></span> <span data-ttu-id="46772-129">L'oggetto **AxWMPLib. AxWindowsMediaPlayer** è rappresentato dalla variabile denominata Player.</span><span class="sxs-lookup"><span data-stu-id="46772-129">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Retrieve a number representing the current proxy settings.
int proxySetting = player.network.getProxySettings("MMS");

// Display the message that corresponds to the current settings.
switch(proxySetting)
{
    case 0:
    proxySettingsLabel.Text = "A proxy server is not being used";
    break;

    case 1: 
    proxySettingsLabel.Text = "The proxy settings for the current browser are being used.";
    break;

    case 2:
    proxySettingsLabel.Text = "The manually specified proxy settings are being used.";
    break;

    case 3:
    proxySettingsLabel.Text = "The proxy settings are being auto-detected.";
    break;

    default:
    proxySettingsLabel.Text = "Unable to determine proxy setting, try again.";
    break;
}
```


```VB

' Retrieve a number representing the current proxy settings.
Dim proxySetting As Integer = player.network.getProxySettings(&quot;MMS&quot;)

&#39; Display the message that corresponds to the current settings.
Select Case proxySetting

    Case 0
        proxySettingsLabel.Text = &quot;A proxy server is not being used&quot;

    Case 1
        proxySettingsLabel.Text = &quot;The proxy settings for the current browser are being used.&quot;

    Case 2
        proxySettingsLabel.Text = &quot;The manually specified proxy settings are being used.&quot;

    Case 3
        proxySettingsLabel.Text = &quot;The proxy settings are being auto-detected.&quot;

    Case Else
        proxySettingsLabel.Text = &quot;Unable to determine proxy setting, try again.&quot;

End Select
```





## <a name="requirements"></a><span data-ttu-id="46772-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46772-130">Requirements</span></span>



| <span data-ttu-id="46772-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="46772-131">Requirement</span></span> | <span data-ttu-id="46772-132">Valore</span><span class="sxs-lookup"><span data-stu-id="46772-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46772-133">Versione</span><span class="sxs-lookup"><span data-stu-id="46772-133">Version</span></span><br/>   | <span data-ttu-id="46772-134">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="46772-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="46772-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46772-135">Namespace</span></span><br/> | <span data-ttu-id="46772-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="46772-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="46772-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="46772-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="46772-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="46772-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46772-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46772-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46772-140">**Interfaccia IWMPNetwork (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="46772-140">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="46772-141">**IWMPNetwork. setProxySettings (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="46772-141">**IWMPNetwork.setProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-setproxysettings--vb-and-c.md)
</dt> </dl>

 

 





