---
title: Metodo Network. getProxyName
description: Il metodo getProxyName Recupera il nome del server proxy in uso.
ms.assetid: 273b1f7d-84b7-4e50-9f80-9fd1978e7528
keywords:
- Metodo getProxyName Media Player Windows
- Metodo getProxyName Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxyName
topic_type:
- apiref
api_name:
- Network.getProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97e51508e9df9aeac85dbc01116e80e710dcb45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328296"
---
# <a name="networkgetproxyname-method"></a><span data-ttu-id="60805-106">Metodo Network. getProxyName</span><span class="sxs-lookup"><span data-stu-id="60805-106">Network.getProxyName method</span></span>

<span data-ttu-id="60805-107">Il metodo **getProxyName** Recupera il nome del server proxy in uso.</span><span class="sxs-lookup"><span data-stu-id="60805-107">The **getProxyName** method retrieves the name of the proxy server being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="60805-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60805-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyName(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="60805-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60805-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60805-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="60805-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60805-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="60805-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="60805-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="60805-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60805-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60805-113">Return value</span></span>

<span data-ttu-id="60805-114">Questo metodo restituisce una **stringa** contenente il nome del server proxy in uso.</span><span class="sxs-lookup"><span data-stu-id="60805-114">This method returns a **String** containing the name of the proxy server being used.</span></span> <span data-ttu-id="60805-115">Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore pari a 2 (usare le impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="60805-115">The value returned is meaningful only when **getProxySettings** returns a value of 2 (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="60805-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="60805-116">Remarks</span></span>

<span data-ttu-id="60805-117">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="60805-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="60805-118">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="60805-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="60805-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="60805-119">Examples</span></span>

<span data-ttu-id="60805-120">Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxyName** per visualizzare i nomi dei server proxy di Windows Media Player per i protocolli http e MMS.</span><span class="sxs-lookup"><span data-stu-id="60805-120">The following JScript example uses *Network*.**getProxyName** to display the Windows Media Player proxy server names for the HTTP and MMS protocols.</span></span> <span data-ttu-id="60805-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="60805-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy server name for HTTP.
   var proxyNameHTTP = Player.network.getProxyName("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy server name for MMS.
   var proxyNameMMS = Player.network.getProxyName("MMS");

// Display the proxy server names in the browser client area.
// Unavailable proxy server names will display as "undefined".
document.write("The current HTTP proxy server name is: " + proxyNameHTTP);
document.write("<BR>");
document.write("The current MMS proxy server name is: " + proxyNameMMS);

```



## <a name="requirements"></a><span data-ttu-id="60805-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60805-122">Requirements</span></span>



| <span data-ttu-id="60805-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60805-123">Requirement</span></span> | <span data-ttu-id="60805-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60805-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="60805-125">Versione</span><span class="sxs-lookup"><span data-stu-id="60805-125">Version</span></span><br/> | <span data-ttu-id="60805-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="60805-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="60805-127">DLL</span><span class="sxs-lookup"><span data-stu-id="60805-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="60805-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60805-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60805-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60805-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60805-130">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="60805-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="60805-131">**Rete. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="60805-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





