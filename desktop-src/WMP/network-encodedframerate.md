---
title: Rete. encodedFrameRate
description: La proprietà encodedFrameRate recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto in frame al secondo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Media Player di Windows Network. encodedFrameRate
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330250"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="a42ef-104">Rete. encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="a42ef-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="a42ef-105">La proprietà **encodedFrameRate** recupera la frequenza dei fotogrammi video specificata dall'autore del contenuto in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="a42ef-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="a42ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a42ef-106">Syntax</span></span>

<span data-ttu-id="a42ef-107">*Player*. *rete*. **encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="a42ef-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a42ef-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="a42ef-108">Possible Values</span></span>

<span data-ttu-id="a42ef-109">Questa proprietà è un **numero** di sola lettura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a42ef-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="a42ef-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="a42ef-110">Examples</span></span>

<span data-ttu-id="a42ef-111">Nell'esempio JScript seguente viene utilizzata la *rete*. **encodedFrameRate** consente di visualizzare la frequenza dei fotogrammi specificata quando il file è stato codificato.</span><span class="sxs-lookup"><span data-stu-id="a42ef-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="a42ef-112">Le informazioni vengono visualizzate in un DIV HTML creato con ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="a42ef-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="a42ef-113">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a42ef-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a42ef-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a42ef-114">Requirements</span></span>



| <span data-ttu-id="a42ef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a42ef-115">Requirement</span></span> | <span data-ttu-id="a42ef-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a42ef-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a42ef-117">Versione</span><span class="sxs-lookup"><span data-stu-id="a42ef-117">Version</span></span><br/> | <span data-ttu-id="a42ef-118">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a42ef-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a42ef-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a42ef-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="a42ef-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a42ef-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a42ef-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a42ef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a42ef-122">**Oggetto di rete**</span><span class="sxs-lookup"><span data-stu-id="a42ef-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a42ef-123">**Rete. frameRate**</span><span class="sxs-lookup"><span data-stu-id="a42ef-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





