---
title: Metodo Network. getProxyExceptionList
description: Il metodo getProxyExceptionList recupera l'elenco di eccezioni del proxy.
ms.assetid: f81d8c0f-cc75-470c-9c24-ceaf8a4b6f97
keywords:
- Metodo getProxyExceptionList Windows Media Player
- Metodo getProxyExceptionList Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxyExceptionList
topic_type:
- apiref
api_name:
- Network.getProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ace9bd569c1cc53a8f3d522703aee6154e68a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331863"
---
# <a name="networkgetproxyexceptionlist-method"></a><span data-ttu-id="f138f-106">Metodo Network. getProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="f138f-106">Network.getProxyExceptionList method</span></span>

<span data-ttu-id="f138f-107">Il metodo **getProxyExceptionList** recupera l'elenco di eccezioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="f138f-107">The **getProxyExceptionList** method retrieves the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f138f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f138f-108">Syntax</span></span>


```JScript
strRetVal = Network.getProxyExceptionList(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="f138f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f138f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f138f-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f138f-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f138f-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="f138f-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="f138f-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="f138f-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f138f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f138f-113">Return value</span></span>

<span data-ttu-id="f138f-114">Questo metodo restituisce una **stringa** che specifica un elenco delimitato da punti e virgola di host per i quali il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="f138f-114">This method returns a **String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="f138f-115">Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore pari a due (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="f138f-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="f138f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f138f-116">Remarks</span></span>

<span data-ttu-id="f138f-117">Si tratta di un elenco di computer, domini e/o indirizzi che ignoreranno il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="f138f-117">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="f138f-118">Il \* carattere può essere usato come carattere jolly per elencare le voci.</span><span class="sxs-lookup"><span data-stu-id="f138f-118">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="f138f-119">Ad esempio, \* . com corrisponde a tutti gli host nel dominio com mentre 67. \* corrisponderebbe a tutti gli host della classe 67 una subnet.</span><span class="sxs-lookup"><span data-stu-id="f138f-119">For example, \*.com would match all hosts in the com domain while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="f138f-120">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="f138f-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="f138f-121">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f138f-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f138f-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="f138f-122">Examples</span></span>

<span data-ttu-id="f138f-123">Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxyExceptionList** per visualizzare gli elenchi di proxy bypassati per i protocolli MMS e http.</span><span class="sxs-lookup"><span data-stu-id="f138f-123">The following JScript example uses *Network*.**getProxyExceptionList** to display the lists of bypassed proxies for the MMS and HTTP protocols.</span></span> <span data-ttu-id="f138f-124">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f138f-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy exception list for HTTP.
   var proxyExceptionListHTTP = Player.network.getProxyExceptionList("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy exception list for MMS.
   var proxyExceptionListMMS = Player.network.getProxyExceptionList("MMS");

// Display the proxy exception lists in the browser client area.
// Unavailable proxy exception lists will display as "undefined".
document.write("The current HTTP proxy exception list: " + proxyExceptionListHTTP);
document.write("<BR>");
document.write("The current MMS proxy exception list: " + proxyExceptionListMMS);

```



## <a name="requirements"></a><span data-ttu-id="f138f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f138f-125">Requirements</span></span>



| <span data-ttu-id="f138f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f138f-126">Requirement</span></span> | <span data-ttu-id="f138f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f138f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f138f-128">Versione</span><span class="sxs-lookup"><span data-stu-id="f138f-128">Version</span></span><br/> | <span data-ttu-id="f138f-129">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f138f-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f138f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f138f-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="f138f-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f138f-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f138f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f138f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f138f-133">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="f138f-133">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="f138f-134">**Rete. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="f138f-134">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





