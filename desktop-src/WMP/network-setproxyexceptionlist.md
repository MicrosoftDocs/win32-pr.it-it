---
title: Metodo Network. setProxyExceptionList
description: Il metodo setProxyExceptionList specifica l'elenco di eccezioni del proxy. | Metodo Network. setProxyExceptionList
ms.assetid: c9eeb058-5ffb-4405-9bf2-776f120e2db4
keywords:
- Metodo setProxyExceptionList Windows Media Player
- Metodo setProxyExceptionList Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxyExceptionList
topic_type:
- apiref
api_name:
- Network.setProxyExceptionList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1e48aa91ec4857181de5c607a586da42d6f2cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324378"
---
# <a name="networksetproxyexceptionlist-method"></a><span data-ttu-id="a752e-107">Metodo Network. setProxyExceptionList</span><span class="sxs-lookup"><span data-stu-id="a752e-107">Network.setProxyExceptionList method</span></span>

<span data-ttu-id="a752e-108">Il metodo **setProxyExceptionList** specifica l'elenco di eccezioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="a752e-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a752e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a752e-109">Syntax</span></span>


```JScript
Network.setProxyExceptionList(
  protocol,
  list
)
```



## <a name="parameters"></a><span data-ttu-id="a752e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a752e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a752e-111">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a752e-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a752e-112">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a752e-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="a752e-113">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a752e-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="a752e-114">*elenco* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a752e-114">*list* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a752e-115">**Stringa** che specifica un elenco delimitato da punti e virgola di host per i quali il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a752e-115">**String** specifying a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a752e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a752e-116">Return value</span></span>

<span data-ttu-id="a752e-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a752e-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a752e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a752e-118">Remarks</span></span>

<span data-ttu-id="a752e-119">Si tratta di un elenco di computer, domini e/o indirizzi che ignoreranno il server proxy quando la parte host dell'URL di destinazione corrisponde a una voce nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="a752e-119">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="a752e-120">Il \* carattere può essere usato come carattere jolly per elencare le voci.</span><span class="sxs-lookup"><span data-stu-id="a752e-120">The \* character can be used as a wildcard for listing entries.</span></span> <span data-ttu-id="a752e-121">Ad esempio, \* . com corrisponde a tutti gli host nel dominio com, mentre 67. \* corrisponderebbe a tutti gli host della classe 67 una subnet.</span><span class="sxs-lookup"><span data-stu-id="a752e-121">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="a752e-122">Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="a752e-122">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="a752e-123">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="a752e-123">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="a752e-124">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a752e-124">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a752e-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="a752e-125">Examples</span></span>

<span data-ttu-id="a752e-126">Nell'esempio JScript seguente viene utilizzata la *rete*. **setProxyExceptionList** per specificare un elenco di host per cui il server proxy viene ignorato quando si utilizza il protocollo MMS.</span><span class="sxs-lookup"><span data-stu-id="a752e-126">The following JScript example uses *Network*.**setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="a752e-127">Il nuovo elenco viene recuperato da un elemento di testo HTML con ID = "XLIST".</span><span class="sxs-lookup"><span data-stu-id="a752e-127">The new list is retrieved from an HTML TEXT element with ID = "XLIST".</span></span> <span data-ttu-id="a752e-128">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a752e-128">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the user's new exception list.
   var proxyxlist = XLIST.value;

   // Set the exception list.
   Player.network.setProxyExceptionList("MMS", proxyxlist);
}

else

// Warn that the proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="a752e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a752e-129">Requirements</span></span>



| <span data-ttu-id="a752e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a752e-130">Requirement</span></span> | <span data-ttu-id="a752e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a752e-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a752e-132">Versione</span><span class="sxs-lookup"><span data-stu-id="a752e-132">Version</span></span><br/> | <span data-ttu-id="a752e-133">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a752e-133">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a752e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a752e-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="a752e-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a752e-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a752e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a752e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a752e-137">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="a752e-137">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





