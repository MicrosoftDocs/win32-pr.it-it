---
title: Metodo Network. seproxyname
description: Il metodo seproxyname specifica il nome del server proxy da usare. | Metodo Network. seproxyname
ms.assetid: dbcb2a00-4387-42af-8055-61d78d021ec7
keywords:
- Metodo seproxyname Media Player Windows
- Metodo seproxyname Media Player Windows, classe di rete
- Classe di rete Windows Media Player, metodo seproxyname
topic_type:
- apiref
api_name:
- Network.setProxyName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a34546a395d48e939c71a806d8125150fca0ff4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329305"
---
# <a name="networksetproxyname-method"></a><span data-ttu-id="93346-107">Metodo Network. seproxyname</span><span class="sxs-lookup"><span data-stu-id="93346-107">Network.setProxyName method</span></span>

<span data-ttu-id="93346-108">Il metodo **Seproxyname** specifica il nome del server proxy da usare.</span><span class="sxs-lookup"><span data-stu-id="93346-108">The **setProxyName** method specifies the name of the proxy server to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="93346-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93346-109">Syntax</span></span>


```JScript
Network.setProxyName(
  protocol,
  name
)
```



## <a name="parameters"></a><span data-ttu-id="93346-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="93346-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93346-111">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="93346-111">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93346-112">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="93346-112">**String** specifying the protocol name.</span></span> <span data-ttu-id="93346-113">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="93346-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="93346-114">*nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93346-114">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93346-115">**Stringa** che specifica il nome del server proxy da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="93346-115">**String** specifying the name of the proxy server to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93346-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93346-116">Return value</span></span>

<span data-ttu-id="93346-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="93346-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93346-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="93346-118">Remarks</span></span>

<span data-ttu-id="93346-119">Questo metodo non ha alcun effetto a meno che **getProxySettings** non restituisca un valore pari a 2 (usare impostazioni manuali).</span><span class="sxs-lookup"><span data-stu-id="93346-119">This method has no effect unless **getProxySettings** returns a value of 2 (use manual settings).</span></span>

<span data-ttu-id="93346-120">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="93346-120">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="93346-121">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="93346-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="93346-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="93346-122">Examples</span></span>

<span data-ttu-id="93346-123">Nell'esempio JScript seguente viene utilizzata la *rete*. **Seproxyname** per specificare il nome del server proxy di Windows Media Player per il protocollo MMS.</span><span class="sxs-lookup"><span data-stu-id="93346-123">The following JScript example uses *Network*.**setProxyName** to specify the name of the Windows Media Player proxy server for the MMS protocol.</span></span> <span data-ttu-id="93346-124">Il nuovo nome viene recuperato da un elemento di testo HTML con ID = "NAME".</span><span class="sxs-lookup"><span data-stu-id="93346-124">The new name is retrieved from an HTML TEXT element with ID = "NAME".</span></span> <span data-ttu-id="93346-125">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="93346-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether proxy settings are manual.
if (Player.network.getProxySettings("MMS") == 2){

   // Store the new proxy server name specified by the user.
   var proxyname = NAME.value;

   // Set the proxy server name.
   Player.network.setProxyName("MMS", proxyname);
}

else

// Warn that proxy settings must be set to 2.
alert("Proxy settings must be manual!");

```



## <a name="requirements"></a><span data-ttu-id="93346-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93346-126">Requirements</span></span>



| <span data-ttu-id="93346-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="93346-127">Requirement</span></span> | <span data-ttu-id="93346-128">Valore</span><span class="sxs-lookup"><span data-stu-id="93346-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="93346-129">Versione</span><span class="sxs-lookup"><span data-stu-id="93346-129">Version</span></span><br/> | <span data-ttu-id="93346-130">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="93346-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="93346-131">DLL</span><span class="sxs-lookup"><span data-stu-id="93346-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="93346-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93346-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93346-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93346-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93346-134">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="93346-134">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





