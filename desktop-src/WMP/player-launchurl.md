---
title: Player. launchURL, metodo
description: Il metodo launchURL Invia un URL al browser predefinito dell'utente di cui eseguire il rendering. | Player. launchURL, metodo
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- Metodo launchURL Windows Media Player
- Metodo launchURL Windows Media Player, classe Player
- Classe Player Windows Media Player, metodo launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326005"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="f0ce9-107">Player. launchURL, metodo</span><span class="sxs-lookup"><span data-stu-id="f0ce9-107">Player.launchURL method</span></span>

<span data-ttu-id="f0ce9-108">Il metodo **launchURL** Invia un URL al browser predefinito dell'utente di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ce9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0ce9-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="f0ce9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0ce9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ce9-111">*URL* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f0ce9-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ce9-112">Valore **stringa** che rappresenta l'URL da avviare.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ce9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0ce9-113">Return value</span></span>

<span data-ttu-id="f0ce9-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0ce9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0ce9-115">Remarks</span></span>

<span data-ttu-id="f0ce9-116">Questo metodo apre solo le pagine Web usando i protocolli HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="f0ce9-117">**Windows Media Player 10 Mobile:** Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="f0ce9-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="f0ce9-118">Examples</span></span>

<span data-ttu-id="f0ce9-119">Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, Visualizza il sito Web Microsoft in una nuova finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="f0ce9-120">L'elemento **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f0ce9-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="f0ce9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0ce9-121">Requirements</span></span>



| <span data-ttu-id="f0ce9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ce9-122">Requirement</span></span> | <span data-ttu-id="f0ce9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f0ce9-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ce9-124">Versione</span><span class="sxs-lookup"><span data-stu-id="f0ce9-124">Version</span></span><br/> | <span data-ttu-id="f0ce9-125">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f0ce9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ce9-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="f0ce9-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ce9-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ce9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0ce9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ce9-129">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="f0ce9-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





