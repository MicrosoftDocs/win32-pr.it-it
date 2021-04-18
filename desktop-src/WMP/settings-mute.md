---
title: Impostazioni. mute
description: La proprietà mute specifica e recupera un valore che indica se l'audio è disattivato.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Settings. mute Media Player Windows
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327379"
---
# <a name="settingsmute"></a><span data-ttu-id="fce26-104">Impostazioni. mute</span><span class="sxs-lookup"><span data-stu-id="fce26-104">Settings.mute</span></span>

<span data-ttu-id="fce26-105">La proprietà **mute** specifica e recupera un valore che indica se l'audio è disattivato.</span><span class="sxs-lookup"><span data-stu-id="fce26-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce26-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fce26-106">Syntax</span></span>

<span data-ttu-id="fce26-107">Player. Settings. mute</span><span class="sxs-lookup"><span data-stu-id="fce26-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="fce26-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="fce26-108">Possible Values</span></span>

<span data-ttu-id="fce26-109">Questa proprietà è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fce26-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="fce26-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fce26-110">Value</span></span> | <span data-ttu-id="fce26-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fce26-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="fce26-112">true</span><span class="sxs-lookup"><span data-stu-id="fce26-112">true</span></span>  | <span data-ttu-id="fce26-113">Audio disattivato.</span><span class="sxs-lookup"><span data-stu-id="fce26-113">Audio is muted.</span></span>              |
| <span data-ttu-id="fce26-114">false</span><span class="sxs-lookup"><span data-stu-id="fce26-114">false</span></span> | <span data-ttu-id="fce26-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="fce26-115">Default.</span></span> <span data-ttu-id="fce26-116">Audio non è disattivato.</span><span class="sxs-lookup"><span data-stu-id="fce26-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="fce26-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="fce26-117">Examples</span></span>

<span data-ttu-id="fce26-118">Nell'esempio seguente viene creato un elemento CHECKBOX HTML che consente all'utente di disattivare e disattivare l'audio.</span><span class="sxs-lookup"><span data-stu-id="fce26-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="fce26-119">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fce26-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="fce26-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fce26-120">Requirements</span></span>



| <span data-ttu-id="fce26-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce26-121">Requirement</span></span> | <span data-ttu-id="fce26-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fce26-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fce26-123">Versione</span><span class="sxs-lookup"><span data-stu-id="fce26-123">Version</span></span><br/> | <span data-ttu-id="fce26-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="fce26-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fce26-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fce26-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fce26-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fce26-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fce26-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fce26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce26-128">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="fce26-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





