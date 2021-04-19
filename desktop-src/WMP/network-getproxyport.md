---
title: Metodo Network. getProxyPort
description: Il metodo getProxyPort recupera la porta proxy utilizzata.
ms.assetid: 76771750-3763-4029-b194-d8567b5f365e
keywords:
- Metodo getProxyPort Windows Media Player
- Metodo getProxyPort Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxyPort
topic_type:
- apiref
api_name:
- Network.getProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3114b2188c0ccb0f6c260df33461fb117e7851e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326330"
---
# <a name="networkgetproxyport-method"></a><span data-ttu-id="cae95-106">Metodo Network. getProxyPort</span><span class="sxs-lookup"><span data-stu-id="cae95-106">Network.getProxyPort method</span></span>

<span data-ttu-id="cae95-107">Il metodo **getProxyPort** recupera la porta proxy utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cae95-107">The **getProxyPort** method retrieves the proxy port being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="cae95-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cae95-108">Syntax</span></span>


```JScript
retVal = Network.getProxyPort(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="cae95-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cae95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae95-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cae95-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cae95-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="cae95-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="cae95-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="cae95-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae95-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cae95-113">Return value</span></span>

<span data-ttu-id="cae95-114">Questo metodo restituisce un **numero** (**Long**) che contiene la porta proxy utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cae95-114">This method returns a **Number** (**long**) containing the proxy port being used.</span></span> <span data-ttu-id="cae95-115">Il valore restituito è significativo solo quando **getProxySettings** restituisce un valore pari a due (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="cae95-115">The value returned is meaningful only when **getProxySettings** returns a value of two (use manual settings).</span></span>

## <a name="remarks"></a><span data-ttu-id="cae95-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="cae95-116">Remarks</span></span>

<span data-ttu-id="cae95-117">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="cae95-117">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="cae95-118">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cae95-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="cae95-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="cae95-119">Examples</span></span>

<span data-ttu-id="cae95-120">Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxyPort** per visualizzare i numeri di porta proxy di Windows Media Player correnti per i protocolli MMS e http.</span><span class="sxs-lookup"><span data-stu-id="cae95-120">The following JScript example uses *Network*.**getProxyPort** to display the current Windows Media Player proxy port numbers for the MMS and HTTP protocols.</span></span> <span data-ttu-id="cae95-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cae95-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the HTTP proxy settings are manual.
if (Player.network.getProxySettings("HTTP") == 2)

   // Get the proxy port number for HTTP.
   var proxyPortHTTP = Player.network.getProxyPort("HTTP");

// Test whether the MMS proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2)

   // Get the proxy port number for MMS.
   var proxyPortMMS = Player.network.getProxyPort("MMS");

// Display the port numbers in the browser client area.
// Unavailable port numbers will display as "undefined".
document.write("The current HTTP proxy port is: " + proxyPortHTTP);
document.write("<BR>");
document.write("The current MMS proxy port is: " + proxyPortMMS);

```



## <a name="requirements"></a><span data-ttu-id="cae95-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cae95-122">Requirements</span></span>



| <span data-ttu-id="cae95-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cae95-123">Requirement</span></span> | <span data-ttu-id="cae95-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cae95-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cae95-125">Versione</span><span class="sxs-lookup"><span data-stu-id="cae95-125">Version</span></span><br/> | <span data-ttu-id="cae95-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="cae95-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cae95-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cae95-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="cae95-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cae95-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae95-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cae95-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cae95-130">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="cae95-130">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="cae95-131">**Rete. getProxySettings**</span><span class="sxs-lookup"><span data-stu-id="cae95-131">**Network.getProxySettings**</span></span>](network-getproxysettings.md)
</dt> </dl>

 

 





