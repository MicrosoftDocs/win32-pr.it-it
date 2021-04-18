---
title: Settings. defaultFrame
description: La proprietà defaultFrame specifica o Recupera il nome del frame usato per visualizzare un URL ricevuto in un evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Impostazioni. defaultFrame Windows Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327982"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="824dd-104">Settings. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="824dd-104">Settings.defaultFrame</span></span>

<span data-ttu-id="824dd-105">La proprietà **DefaultFrame** specifica o Recupera il nome del frame usato per visualizzare un URL ricevuto in un evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="824dd-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="824dd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="824dd-106">Syntax</span></span>

<span data-ttu-id="824dd-107">Player. Settings. defaultFrame</span><span class="sxs-lookup"><span data-stu-id="824dd-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="824dd-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="824dd-108">Possible Values</span></span>

<span data-ttu-id="824dd-109">Questa proprietà è una **stringa** di lettura/scrittura che corrisponde al valore dell'attributo **Name** dell'elemento frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="824dd-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="824dd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="824dd-110">Remarks</span></span>

<span data-ttu-id="824dd-111">Se un frame di destinazione viene specificato nell'evento **ScriptCommand** stesso, questa proprietà viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="824dd-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="824dd-112">Questa proprietà viene ignorata quando si usa l'applet Java del navigatore Netscape.</span><span class="sxs-lookup"><span data-stu-id="824dd-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="824dd-113">In Navigator ogni comando script URL ricevuto Visualizza l'URL in una nuova finestra del browser, indipendentemente dal valore delle *Impostazioni*. **DefaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="824dd-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="824dd-114">**Windows Media Player 10 Mobile**: questa proprietà è di sola lettura e restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="824dd-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="824dd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="824dd-115">Requirements</span></span>



| <span data-ttu-id="824dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="824dd-116">Requirement</span></span> | <span data-ttu-id="824dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="824dd-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="824dd-118">Versione</span><span class="sxs-lookup"><span data-stu-id="824dd-118">Version</span></span><br/> | <span data-ttu-id="824dd-119">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="824dd-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="824dd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="824dd-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="824dd-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="824dd-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="824dd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="824dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824dd-123">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="824dd-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="824dd-124">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="824dd-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="824dd-125">**Uso di Windows Media Player con Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="824dd-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





