---
title: Metodo Network. setProxySettings
description: Il metodo setProxySettings specifica l'impostazione del proxy per un protocollo specificato.
ms.assetid: 473501c9-27ea-47ec-bc82-691804fbfb89
keywords:
- Metodo setProxySettings Windows Media Player
- Metodo setProxySettings Media Player Windows, classe di rete
- Classe di rete Media Player Windows, metodo setProxySettings
topic_type:
- apiref
api_name:
- Network.setProxySettings
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f3da665b07f717449721c9fb43a8733cdb6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325439"
---
# <a name="networksetproxysettings-method"></a><span data-ttu-id="a08d2-106">Metodo Network. setProxySettings</span><span class="sxs-lookup"><span data-stu-id="a08d2-106">Network.setProxySettings method</span></span>

<span data-ttu-id="a08d2-107">Il metodo **setProxySettings** specifica l'impostazione del proxy per un protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="a08d2-107">The **setProxySettings** method specifies the proxy setting for a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="a08d2-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a08d2-108">Syntax</span></span>


```JScript
Network.setProxySettings(
  protocol,
  setting
)
```



## <a name="parameters"></a><span data-ttu-id="a08d2-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a08d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a08d2-110">*protocollo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a08d2-110">*protocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08d2-111">**Stringa** che specifica il nome del protocollo.</span><span class="sxs-lookup"><span data-stu-id="a08d2-111">**String** specifying the protocol name.</span></span> <span data-ttu-id="a08d2-112">Per un elenco di protocolli supportati, vedere [protocolli e tipi di file supportati](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a08d2-112">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="a08d2-113">*impostazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a08d2-113">*setting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a08d2-114">**Numero** (**Long**) contenente uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a08d2-114">**Number** (**long**) containing one of the following values.</span></span>



| <span data-ttu-id="a08d2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a08d2-115">Value</span></span> | <span data-ttu-id="a08d2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a08d2-116">Description</span></span>                                                          |
|-------|----------------------------------------------------------------------|
| <span data-ttu-id="a08d2-117">0</span><span class="sxs-lookup"><span data-stu-id="a08d2-117">0</span></span>     | <span data-ttu-id="a08d2-118">Non usare un server proxy.</span><span class="sxs-lookup"><span data-stu-id="a08d2-118">Do not use a proxy server.</span></span>                                           |
| <span data-ttu-id="a08d2-119">1</span><span class="sxs-lookup"><span data-stu-id="a08d2-119">1</span></span>     | <span data-ttu-id="a08d2-120">Usare le impostazioni proxy del browser corrente (valido solo per HTTP).</span><span class="sxs-lookup"><span data-stu-id="a08d2-120">Use the proxy settings of the current browser (only valid for HTTP).</span></span> |
| <span data-ttu-id="a08d2-121">2</span><span class="sxs-lookup"><span data-stu-id="a08d2-121">2</span></span>     | <span data-ttu-id="a08d2-122">Usare le impostazioni proxy specificate manualmente.</span><span class="sxs-lookup"><span data-stu-id="a08d2-122">Use the manually specified proxy settings.</span></span>                           |
| <span data-ttu-id="a08d2-123">3</span><span class="sxs-lookup"><span data-stu-id="a08d2-123">3</span></span>     | <span data-ttu-id="a08d2-124">Rilevare automaticamente le impostazioni del proxy.</span><span class="sxs-lookup"><span data-stu-id="a08d2-124">Auto-detect the proxy settings.</span></span>                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a08d2-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a08d2-125">Return value</span></span>

<span data-ttu-id="a08d2-126">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a08d2-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a08d2-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a08d2-127">Remarks</span></span>

<span data-ttu-id="a08d2-128">Questo metodo ha esito negativo a meno che l'applicazione chiamante non sia in esecuzione nel computer locale o nella Intranet.</span><span class="sxs-lookup"><span data-stu-id="a08d2-128">This method fails unless the calling application is running on the local computer or intranet.</span></span>

<span data-ttu-id="a08d2-129">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a08d2-129">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="a08d2-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="a08d2-130">Examples</span></span>

<span data-ttu-id="a08d2-131">Nell'esempio seguente viene utilizzato JScript con un elemento HTML SELECT **per consentire all'utente di specificare l'impostazione del proxy di Windows Media Player per il protocollo http. L'oggetto Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a08d2-131">The following example uses JScript with an HTML SELECT **element to allow the user to specify the Windows Media Player proxy setting for the HTTP protocol. The Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = HTTPsetproxy  NAME = "HTTPsetproxy"  LANGUAGE="JScript"
        onChange = "
                      /* Store the current selection.*/
                      var setting = this.value;

                      /* Change the proxy setting. */
                      Player.network.setProxySettings('HTTP', setting);
">

<OPTION VALUE=0>Do not use a proxy server
<OPTION VALUE=1>Use the browser settings
<OPTION VALUE=2>Use manual settings
<OPTION VALUE=3>Auto-detect settings

</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="a08d2-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a08d2-132">Requirements</span></span>



| <span data-ttu-id="a08d2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a08d2-133">Requirement</span></span> | <span data-ttu-id="a08d2-134">Valore</span><span class="sxs-lookup"><span data-stu-id="a08d2-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a08d2-135">Versione</span><span class="sxs-lookup"><span data-stu-id="a08d2-135">Version</span></span><br/> | <span data-ttu-id="a08d2-136">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a08d2-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a08d2-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a08d2-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="a08d2-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a08d2-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a08d2-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a08d2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a08d2-140">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="a08d2-140">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





