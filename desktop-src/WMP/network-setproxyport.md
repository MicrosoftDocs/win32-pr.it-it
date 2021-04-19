---
title: Metodo Network. setProxyPort
description: Il metodo setProxyPort specifica la porta proxy da usare. | Metodo Network. setProxyPort
ms.assetid: 09cfce4a-191c-4596-b678-15d9328d5c53
keywords:
- Metodo setProxyPort Windows Media Player
- Metodo setProxyPort Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxyPort
topic_type:
- apiref
api_name:
- Network.setProxyPort
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2438688535e4727688ddbd5d67fd65cbed15864d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324088"
---
# <a name="networksetproxyport-method"></a><span data-ttu-id="165e4-107">Metodo Network. setProxyPort</span><span class="sxs-lookup"><span data-stu-id="165e4-107">Network.setProxyPort method</span></span>

<span data-ttu-id="165e4-108">Il metodo **setProxyPort** specifica la porta proxy da usare.</span><span class="sxs-lookup"><span data-stu-id="165e4-108">The **setProxyPort** method specifies the proxy port to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="165e4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="165e4-109">Syntax</span></span>


```JScript
Network.setProxyPort(
  protocol,
  port
)
```



## <a name="parameters"></a><span data-ttu-id="165e4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="165e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="165e4-111">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="165e4-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="165e4-112">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="165e4-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="165e4-113">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="165e4-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="165e4-114">*porta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="165e4-114">*port* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="165e4-115">**Numero** (**Long**) che specifica la porta del proxy da usare.</span><span class="sxs-lookup"><span data-stu-id="165e4-115">**Number** (**long**) specifying the proxy port to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="165e4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="165e4-116">Return value</span></span>

<span data-ttu-id="165e4-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="165e4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="165e4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="165e4-118">Remarks</span></span>

<span data-ttu-id="165e4-119">Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="165e4-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="165e4-120">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="165e4-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="165e4-121">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="165e4-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="165e4-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="165e4-122">Examples</span></span>

<span data-ttu-id="165e4-123">Nell'esempio JScript seguente viene utilizzata la *rete*. **setProxyPort** per specificare il numero di porta del proxy di Windows Media Player per il protocollo MMS.</span><span class="sxs-lookup"><span data-stu-id="165e4-123">The following JScript example uses *Network*.**setProxyPort** to specify the Windows Media Player proxy port number for the MMS protocol.</span></span> <span data-ttu-id="165e4-124">Il numero di porta viene recuperato da un elemento INPUT HTML con ID = "PORT".</span><span class="sxs-lookup"><span data-stu-id="165e4-124">The port number is retrieved from an HTML INPUT element with ID = "PORT".</span></span> <span data-ttu-id="165e4-125">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="165e4-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the port number specified by the user.
   var portnumber = PORT.value;

   // Set the port number for the MMS protocol.
   Player.network.setProxyPort("MMS", portnumber);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="165e4-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="165e4-126">Requirements</span></span>



| <span data-ttu-id="165e4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="165e4-127">Requirement</span></span> | <span data-ttu-id="165e4-128">Valore</span><span class="sxs-lookup"><span data-stu-id="165e4-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="165e4-129">Versione</span><span class="sxs-lookup"><span data-stu-id="165e4-129">Version</span></span><br/> | <span data-ttu-id="165e4-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="165e4-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="165e4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="165e4-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="165e4-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="165e4-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165e4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="165e4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165e4-134">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="165e4-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





