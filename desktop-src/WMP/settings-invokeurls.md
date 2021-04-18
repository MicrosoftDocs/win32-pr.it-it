---
title: Settings. invokeURLs
description: La proprietà invokeURLs specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Impostazioni. invokeURLs Windows Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327383"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="85e7c-104">Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="85e7c-104">Settings.invokeURLs</span></span>

<span data-ttu-id="85e7c-105">La proprietà **invokeURLs** specifica o recupera un valore che indica se gli eventi URL devono avviare un Web browser.</span><span class="sxs-lookup"><span data-stu-id="85e7c-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="85e7c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85e7c-106">Syntax</span></span>

<span data-ttu-id="85e7c-107">Player. Settings. invokeURLs</span><span class="sxs-lookup"><span data-stu-id="85e7c-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="85e7c-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="85e7c-108">Possible Values</span></span>

<span data-ttu-id="85e7c-109">Questa proprietà è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="85e7c-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="85e7c-110">Valore</span><span class="sxs-lookup"><span data-stu-id="85e7c-110">Value</span></span> | <span data-ttu-id="85e7c-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85e7c-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="85e7c-112">true</span><span class="sxs-lookup"><span data-stu-id="85e7c-112">true</span></span>  | <span data-ttu-id="85e7c-113">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="85e7c-113">Default.</span></span> <span data-ttu-id="85e7c-114">Gli eventi URL dovrebbero avviare un browser.</span><span class="sxs-lookup"><span data-stu-id="85e7c-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="85e7c-115">false</span><span class="sxs-lookup"><span data-stu-id="85e7c-115">false</span></span> | <span data-ttu-id="85e7c-116">Gli eventi URL non devono avviare un browser.</span><span class="sxs-lookup"><span data-stu-id="85e7c-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="85e7c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="85e7c-117">Remarks</span></span>

<span data-ttu-id="85e7c-118">I file multimediali possono contenere URL.</span><span class="sxs-lookup"><span data-stu-id="85e7c-118">Media files can contain URLs.</span></span> <span data-ttu-id="85e7c-119">Quando un URL viene inviato al controllo Media Player di Windows, viene passato prima al gestore eventi **ScriptCommand** , indipendentemente dal valore in **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="85e7c-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="85e7c-120">Dopo la chiusura di **ScriptCommand** , Windows Media Player controlla **invokeURLs** per determinare se avviare il browser Internet predefinito con l'URL.</span><span class="sxs-lookup"><span data-stu-id="85e7c-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="85e7c-121">È possibile visualizzare gli URL in modo selettivo e selezionarli in **ScriptCommand** e impostare **invokeURLs** come desiderato.</span><span class="sxs-lookup"><span data-stu-id="85e7c-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="85e7c-122">**Windows Media Player 10 Mobile**: questa proprietà accetta o restituisce false.</span><span class="sxs-lookup"><span data-stu-id="85e7c-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="85e7c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85e7c-123">Requirements</span></span>



| <span data-ttu-id="85e7c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="85e7c-124">Requirement</span></span> | <span data-ttu-id="85e7c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="85e7c-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85e7c-126">Versione</span><span class="sxs-lookup"><span data-stu-id="85e7c-126">Version</span></span><br/> | <span data-ttu-id="85e7c-127">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="85e7c-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="85e7c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="85e7c-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="85e7c-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85e7c-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85e7c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85e7c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85e7c-131">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="85e7c-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="85e7c-132">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="85e7c-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





