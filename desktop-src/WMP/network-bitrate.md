---
title: Rete. bitrate
description: La proprietà bitrate recupera la velocità in bit corrente ricevuta.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Media Player Windows di rete. bitrate
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326120"
---
# <a name="networkbitrate"></a><span data-ttu-id="3325c-104">Rete. bitrate</span><span class="sxs-lookup"><span data-stu-id="3325c-104">Network.bitRate</span></span>

<span data-ttu-id="3325c-105">La proprietà **bitrate** recupera la velocità in bit corrente ricevuta.</span><span class="sxs-lookup"><span data-stu-id="3325c-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="3325c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3325c-106">Syntax</span></span>

<span data-ttu-id="3325c-107">*Player*. *rete*. **velocità in bit**</span><span class="sxs-lookup"><span data-stu-id="3325c-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3325c-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="3325c-108">Possible Values</span></span>

<span data-ttu-id="3325c-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="3325c-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3325c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3325c-110">Remarks</span></span>

<span data-ttu-id="3325c-111">Questo valore è una combinazione della velocità in bit dei flussi video e audio correnti.</span><span class="sxs-lookup"><span data-stu-id="3325c-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="3325c-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="3325c-112">Examples</span></span>

<span data-ttu-id="3325c-113">Nell'esempio JScript seguente viene utilizzata la *rete*. **bitrate** per visualizzare la velocità in bit dei supporti correnti.</span><span class="sxs-lookup"><span data-stu-id="3325c-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="3325c-114">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "BR".</span><span class="sxs-lookup"><span data-stu-id="3325c-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="3325c-115">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="3325c-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="3325c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3325c-116">Requirements</span></span>



| <span data-ttu-id="3325c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3325c-117">Requirement</span></span> | <span data-ttu-id="3325c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3325c-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3325c-119">Versione</span><span class="sxs-lookup"><span data-stu-id="3325c-119">Version</span></span><br/> | <span data-ttu-id="3325c-120">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="3325c-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3325c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3325c-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="3325c-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3325c-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3325c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3325c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3325c-124">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="3325c-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





