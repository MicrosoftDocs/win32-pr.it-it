---
title: Rete. sourceProtocol
description: La proprietà sourceProtocol Recupera il protocollo di origine utilizzato per la ricezione dei dati.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Media Player di Windows Network. sourceProtocol
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326329"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="77e1b-104">Rete. sourceProtocol</span><span class="sxs-lookup"><span data-stu-id="77e1b-104">Network.sourceProtocol</span></span>

<span data-ttu-id="77e1b-105">La proprietà **sourceProtocol** Recupera il protocollo di origine utilizzato per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="77e1b-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="77e1b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77e1b-106">Syntax</span></span>

<span data-ttu-id="77e1b-107">*Player*. *rete*. **sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="77e1b-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="77e1b-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="77e1b-108">Possible Values</span></span>

<span data-ttu-id="77e1b-109">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="77e1b-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="77e1b-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="77e1b-110">Remarks</span></span>

<span data-ttu-id="77e1b-111">Questa proprietà è impostata su "" (stringa vuota) quando si esegue la riproduzione di file multimediali da un CD o un DVD.</span><span class="sxs-lookup"><span data-stu-id="77e1b-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="77e1b-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="77e1b-112">Examples</span></span>

<span data-ttu-id="77e1b-113">Nell'esempio JScript seguente viene utilizzata la *rete*. **sourceProtocol** per visualizzare il protocollo di origine utilizzato per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="77e1b-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="77e1b-114">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "SP".</span><span class="sxs-lookup"><span data-stu-id="77e1b-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="77e1b-115">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="77e1b-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="77e1b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77e1b-116">Requirements</span></span>



| <span data-ttu-id="77e1b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="77e1b-117">Requirement</span></span> | <span data-ttu-id="77e1b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="77e1b-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77e1b-119">Versione</span><span class="sxs-lookup"><span data-stu-id="77e1b-119">Version</span></span><br/> | <span data-ttu-id="77e1b-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="77e1b-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="77e1b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="77e1b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="77e1b-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77e1b-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77e1b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77e1b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77e1b-124">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="77e1b-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





