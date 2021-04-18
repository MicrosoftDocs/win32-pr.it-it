---
title: Player. windowlessVideo
description: La proprietà windowlessVideo specifica o recupera un valore che indica se il controllo di Windows Media Player esegue il rendering del video in modalità senza finestra.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player. windowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327054"
---
# <a name="playerwindowlessvideo"></a><span data-ttu-id="9a908-104">Player. windowlessVideo</span><span class="sxs-lookup"><span data-stu-id="9a908-104">Player.windowlessVideo</span></span>

<span data-ttu-id="9a908-105">La proprietà **windowlessVideo** specifica o recupera un valore che indica se il controllo di Windows Media Player esegue il rendering del video in modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="9a908-105">The **windowlessVideo** property specifies or retrieves a value indicating whether the Windows Media Player control renders video in windowless mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a908-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a908-106">Syntax</span></span>

<span data-ttu-id="9a908-107">*Player*. **windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="9a908-107">*player*.**windowlessVideo**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9a908-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="9a908-108">Possible Values</span></span>

<span data-ttu-id="9a908-109">Questa proprietà è un **valore booleano** che viene specificato in fase di progettazione ed è successivamente di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9a908-109">This property is a **Boolean** that is specified at design time and is read-only thereafter.</span></span>



| <span data-ttu-id="9a908-110">Valore</span><span class="sxs-lookup"><span data-stu-id="9a908-110">Value</span></span> | <span data-ttu-id="9a908-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a908-111">Description</span></span>                                      |
|-------|--------------------------------------------------|
| <span data-ttu-id="9a908-112">true</span><span class="sxs-lookup"><span data-stu-id="9a908-112">true</span></span>  | <span data-ttu-id="9a908-113">Il video viene sottoposto a rendering in modalità senza finestra.</span><span class="sxs-lookup"><span data-stu-id="9a908-113">The video is rendered in windowless mode.</span></span>        |
| <span data-ttu-id="9a908-114">false</span><span class="sxs-lookup"><span data-stu-id="9a908-114">false</span></span> | <span data-ttu-id="9a908-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="9a908-115">Default.</span></span> <span data-ttu-id="9a908-116">Il video viene sottoposto a rendering in modalità finestra.</span><span class="sxs-lookup"><span data-stu-id="9a908-116">The video is rendered in windowed mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9a908-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9a908-117">Remarks</span></span>

<span data-ttu-id="9a908-118">Per impostazione predefinita, un controllo di Windows Media Player incorporato esegue il rendering dei video nella propria finestra all'interno dell'area client.</span><span class="sxs-lookup"><span data-stu-id="9a908-118">By default, an embedded Windows Media Player control renders video in its own window within the client area.</span></span> <span data-ttu-id="9a908-119">Quando **windowlessVideo** è impostato su true, il controllo Player esegue il rendering del video direttamente nell'area client, in modo che sia possibile applicare effetti speciali o sovrapporre il video con il testo.</span><span class="sxs-lookup"><span data-stu-id="9a908-119">When **windowlessVideo** is set to true, the Player control renders video directly in the client area, so you can apply special effects or layer the video with text.</span></span>

<span data-ttu-id="9a908-120">In Windows Vista, il rendering di video in modalità senza finestra può compromettere le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="9a908-120">In Windows Vista, rendering video in windowless mode can degrade performance.</span></span>

<span data-ttu-id="9a908-121">La proprietà **windowlessVideo** non è supportata per il navigatore Netscape.</span><span class="sxs-lookup"><span data-stu-id="9a908-121">The **windowlessVideo** property is not supported for Netscape Navigator.</span></span> <span data-ttu-id="9a908-122">L'impostazione di un valore per questa proprietà in Navigator può produrre risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="9a908-122">Setting a value for this property in Navigator may yield unexpected results.</span></span>

<span data-ttu-id="9a908-123">**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9a908-123">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a908-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a908-124">Requirements</span></span>



| <span data-ttu-id="9a908-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a908-125">Requirement</span></span> | <span data-ttu-id="9a908-126">Valore</span><span class="sxs-lookup"><span data-stu-id="9a908-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9a908-127">Versione</span><span class="sxs-lookup"><span data-stu-id="9a908-127">Version</span></span><br/> | <span data-ttu-id="9a908-128">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9a908-128">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="9a908-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9a908-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a908-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a908-130"><dt>Wmp.dll</dt></span></span> </dl> |



 

 





