---
title: Metodo Network. setProxyBypassForLocal
description: Il metodo setProxyBypassForLocal specifica un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.
ms.assetid: 3023a561-f3b7-45c8-a432-baadd795aaa6
keywords:
- Metodo setProxyBypassForLocal Windows Media Player
- Metodo setProxyBypassForLocal Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxyBypassForLocal
topic_type:
- apiref
api_name:
- Network.setProxyBypassForLocal
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9426c310c8977317cf5a8415fd19966b8dfc8fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328713"
---
# <a name="networksetproxybypassforlocal-method"></a><span data-ttu-id="1ff26-106">Metodo Network. setProxyBypassForLocal</span><span class="sxs-lookup"><span data-stu-id="1ff26-106">Network.setProxyBypassForLocal method</span></span>

<span data-ttu-id="1ff26-107">Il metodo **setProxyBypassForLocal** specifica un valore che indica se il server proxy viene ignorato se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="1ff26-107">The **setProxyBypassForLocal** method specifies a value indicating whether the proxy server is bypassed if the origin server is on a local network.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff26-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ff26-108">Syntax</span></span>


```JScript
Network.setProxyBypassForLocal(
  protocol,
  bypass
)
```



## <a name="parameters"></a><span data-ttu-id="1ff26-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ff26-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff26-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1ff26-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff26-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="1ff26-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="1ff26-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1ff26-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ff26-113">*Ignora* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ff26-113">*bypass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff26-114">**Valore booleano** che specifica se il server proxy viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1ff26-114">**Boolean** specifying whether the proxy server is bypassed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff26-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ff26-115">Return value</span></span>

<span data-ttu-id="1ff26-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1ff26-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ff26-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ff26-117">Remarks</span></span>

<span data-ttu-id="1ff26-118">Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="1ff26-118">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="1ff26-119">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="1ff26-119">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="1ff26-120">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1ff26-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="1ff26-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="1ff26-121">Examples</span></span>

<span data-ttu-id="1ff26-122">Nell'esempio JScript seguente viene utilizzata la *rete*. **setProxyBypassForLocal** consente di specificare se il server proxy di Windows Media Player viene ignorato, quando si utilizza il protocollo MMS se il server di origine si trova in una rete locale.</span><span class="sxs-lookup"><span data-stu-id="1ff26-122">The following JScript example uses *Network*.**setProxyBypassForLocal** to specify whether the Windows Media Player proxy server is bypassed, when using the MMS protocol, if the origin server is on a local network.</span></span> <span data-ttu-id="1ff26-123">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1ff26-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Prompt the user for a setting. Store the response in a variable.
   var proxybypass = confirm("Bypass proxy server for local addresses? \n OK = Yes \n Cancel = No");

   // Set the proxy bypass value using the user input.
   Player.network.setProxyBypassForLocal("MMS", proxybypass);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="1ff26-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ff26-124">Requirements</span></span>



| <span data-ttu-id="1ff26-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ff26-125">Requirement</span></span> | <span data-ttu-id="1ff26-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1ff26-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff26-127">Versione</span><span class="sxs-lookup"><span data-stu-id="1ff26-127">Version</span></span><br/> | <span data-ttu-id="1ff26-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="1ff26-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1ff26-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1ff26-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ff26-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ff26-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff26-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ff26-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff26-132">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="1ff26-132">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





