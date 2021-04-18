---
title: Metodo Network. getProxyBypassForLocal
description: Il metodo getProxyBypassForLocal recupera un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.
ms.assetid: e5217d56-da22-4424-94b0-400369410b47
keywords:
- Metodo getProxyBypassForLocal Windows Media Player
- Metodo getProxyBypassForLocal Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.getProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c60b9248cd5a893496c2de88c5a5370dfb7bf82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327483"
---
# <a name="networkgetproxybypassforlocal-method"></a><span data-ttu-id="ec762-106">Metodo Network. getProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="ec762-106">Network.getProxyBypassForLocal method</span></span>

<span data-ttu-id="ec762-107">Il metodo **getProxyBypassForLocal** recupera un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="ec762-107">The **getProxyBypassForLocal** method retrieves a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec762-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec762-108">Syntax</span></span>


```JScript
bRetVal = Network.getProxyBypassForLocal(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="ec762-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec762-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec762-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ec762-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec762-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="ec762-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="ec762-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="ec762-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec762-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec762-113">Return value</span></span>

<span data-ttu-id="ec762-114">Questo metodo restituisce un **valore booleano** che indica se il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ec762-114">This method returns a **Boolean** indicating whether the proxy server is bypassed.</span></span> <span data-ttu-id="ec762-115">Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore pari a due (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="ec762-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec762-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec762-116">Remarks</span></span>

<span data-ttu-id="ec762-117">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="ec762-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="ec762-118">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ec762-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="ec762-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec762-119">Examples</span></span>

<span data-ttu-id="ec762-120">Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxyBypassForLocal** per visualizzare se Windows Media Player è impostato in modo da ignorare il server proxy per gli indirizzi locali.</span><span class="sxs-lookup"><span data-stu-id="ec762-120">The following JScript example uses *Network*.**getProxyBypassForLocal** to display whether Windows Media Player is set to bypass the proxy server for local addresses.</span></span> <span data-ttu-id="ec762-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ec762-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy bypass for local value for HTTP.
   var proxyBypassForLocalHTTP = Player.network.getProxyBypassForLocal("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy bypass for local value for MMS.
   var proxyBypassForLocalMMS = Player.network.getProxyBypassForLocal("MMS");

// Display the proxy bypass for local values in the browser client area.
// Unavailable proxy bypass for local values will display as "undefined".
document.write("The current HTTP proxy bypass for local value: " + proxyBypassForLocalHTTP);
document.write("<BR>");
document.write("The current MMS proxy bypass for local value: " + proxyBypassForLocalMMS);

```



## <a name="requirements"></a><span data-ttu-id="ec762-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec762-122">Requirements</span></span>



| <span data-ttu-id="ec762-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec762-123">Requirement</span></span> | <span data-ttu-id="ec762-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ec762-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec762-125">Versione</span><span class="sxs-lookup"><span data-stu-id="ec762-125">Version</span></span><br/> | <span data-ttu-id="ec762-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="ec762-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ec762-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ec762-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="ec762-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec762-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec762-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec762-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec762-130">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="ec762-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="ec762-131">**Rete. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="ec762-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





