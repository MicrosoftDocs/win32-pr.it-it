---
title: Metodo Network. getProxySettings
description: Il metodo getProxySettings recupera l'impostazione del proxy per un protocollo specificato.
ms.assetid: a7b21eab-93e1-458b-aab0-60fd298cce44
keywords:
- Metodo getProxySettings Windows Media Player
- Metodo getProxySettings Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo getProxySettings
topic_type:
- apiref
api_name:
- Network.getProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44a306fca1e671e7e5b3a89c0da952e5c81ba20e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328295"
---
# <a name="networkgetproxysettings-method"></a><span data-ttu-id="50433-106">Metodo Network. getProxySettings</span><span class="sxs-lookup"><span data-stu-id="50433-106">Network.getProxySettings method</span></span>

<span data-ttu-id="50433-107">Il metodo **getProxySettings** recupera l'impostazione del proxy per un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="50433-107">The **getProxySettings** method retrieves the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="50433-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50433-108">Syntax</span></span>


```JScript
retVal = Network.getProxySettings(
  protocol
)
```



## <a name="parameters"></a><span data-ttu-id="50433-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="50433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50433-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="50433-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50433-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="50433-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="50433-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="50433-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50433-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50433-113">Return value</span></span>

<span data-ttu-id="50433-114">Questo metodo restituisce un **numero** (**Long**) contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="50433-114">This method returns a **Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="50433-115">Valore</span><span class="sxs-lookup"><span data-stu-id="50433-115">Value</span></span> | <span data-ttu-id="50433-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50433-116">Description</span></span>                                                                      |
|-------|----------------------------------------------------------------------------------|
| <span data-ttu-id="50433-117">0</span><span class="sxs-lookup"><span data-stu-id="50433-117">0</span></span>     | <span data-ttu-id="50433-118">Non è in uso un server proxy.</span><span class="sxs-lookup"><span data-stu-id="50433-118">A proxy server is not being used.</span></span>                                                |
| <span data-ttu-id="50433-119">1</span><span class="sxs-lookup"><span data-stu-id="50433-119">1</span></span>     | <span data-ttu-id="50433-120">Vengono usate le impostazioni proxy per il browser corrente (valido solo per HTTP).</span><span class="sxs-lookup"><span data-stu-id="50433-120">The proxy settings for the current browser are being used (only valid for HTTP).</span></span> |
| <span data-ttu-id="50433-121">2</span><span class="sxs-lookup"><span data-stu-id="50433-121">2</span></span>     | <span data-ttu-id="50433-122">Sono in uso le impostazioni proxy specificate manualmente.</span><span class="sxs-lookup"><span data-stu-id="50433-122">The manually specified proxy settings are being used.</span></span>                            |
| <span data-ttu-id="50433-123">3</span><span class="sxs-lookup"><span data-stu-id="50433-123">3</span></span>     | <span data-ttu-id="50433-124">Le impostazioni proxy vengono rilevate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="50433-124">The proxy settings are being auto-detected.</span></span>                                      |



 

## <a name="remarks"></a><span data-ttu-id="50433-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="50433-125">Remarks</span></span>

<span data-ttu-id="50433-126">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="50433-126">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="50433-127">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="50433-127">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="50433-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="50433-128">Examples</span></span>

<span data-ttu-id="50433-129">Nell'esempio JScript seguente viene utilizzata la *rete*. **getProxySettings** per visualizzare un messaggio, che fornisce informazioni sulle impostazioni proxy correnti del lettore, nella finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="50433-129">The following JScript example uses *Network*.**getProxySettings** to display a message, which gives information about the current proxy settings of the Player, in the browser window.</span></span> <span data-ttu-id="50433-130">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="50433-130">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve a number representing the current proxy settings.
var proxySetting = Player.network.getProxySettings("MMS");

// Display the message the corresponds to the current settings.
switch(proxySetting){

   case 0:
     document.write("A proxy server is not being used");
     break;

   case 1: 
     document.write("The proxy settings for the current browser are being used.");
     break;

   case 2:
     document.write("The manually specified proxy settings are being used.");
     break;

case 3:
     document.write("The proxy settings are being auto-detected.");
     break;

   default:
     document.write("Unable to determine proxy setting, try again.");
}

```



## <a name="requirements"></a><span data-ttu-id="50433-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50433-131">Requirements</span></span>



| <span data-ttu-id="50433-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="50433-132">Requirement</span></span> | <span data-ttu-id="50433-133">Valore</span><span class="sxs-lookup"><span data-stu-id="50433-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50433-134">Versione</span><span class="sxs-lookup"><span data-stu-id="50433-134">Version</span></span><br/> | <span data-ttu-id="50433-135">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="50433-135">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="50433-136">DLL</span><span class="sxs-lookup"><span data-stu-id="50433-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="50433-137"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50433-137"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50433-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50433-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50433-139">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="50433-139">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





