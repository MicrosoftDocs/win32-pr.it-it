---
title: Settings. baseURL
description: La proprietà baseURL specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati negli elementi multimediali.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Impostazioni. baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325132"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="29eed-104">Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="29eed-104">Settings.baseURL</span></span>

<span data-ttu-id="29eed-105">La proprietà **BaseUrl** specifica o recupera l'URL di base usato per la risoluzione del percorso relativo con i comandi script URL incorporati negli elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="29eed-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="29eed-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29eed-106">Syntax</span></span>

<span data-ttu-id="29eed-107">Player. Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="29eed-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="29eed-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="29eed-108">Possible Values</span></span>

<span data-ttu-id="29eed-109">Questa proprietà è una **stringa** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="29eed-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="29eed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="29eed-110">Remarks</span></span>

<span data-ttu-id="29eed-111">Questa proprietà specifica l'URL HTTP di base che viene passato come parametro Command dall'evento **ScriptCommand** .</span><span class="sxs-lookup"><span data-stu-id="29eed-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="29eed-112">L'URL di base viene concatenato all'URL relativo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="29eed-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="29eed-113">Viene aggiunta una barra (/) finale al valore della proprietà **BaseUrl** .</span><span class="sxs-lookup"><span data-stu-id="29eed-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="29eed-114">Un punto, una barra rovesciata o una barra (., \\ e/) iniziali vengono eliminati dall'URL relativo.</span><span class="sxs-lookup"><span data-stu-id="29eed-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="29eed-115">L'URL relativo viene aggiunto alla fine dell'URL di base.</span><span class="sxs-lookup"><span data-stu-id="29eed-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="29eed-116">Tutte le barre nell'URL completo risultante sono posizionate nella stessa direzione (convertite in avanti o in barre rovesciate) in base alla direzione del primo carattere barra rilevato nel nuovo URL.</span><span class="sxs-lookup"><span data-stu-id="29eed-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="29eed-117">**Nota**</span><span class="sxs-lookup"><span data-stu-id="29eed-117">**Note**</span></span>

<span data-ttu-id="29eed-118">Il controllo Player non supporta l'utilizzo di due punti (..) nell'URL relativo per indicare l'elemento padre della posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="29eed-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="29eed-119">**Windows Media Player 10 Mobile**: questa proprietà è di sola lettura e restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="29eed-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="29eed-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29eed-120">Requirements</span></span>



| <span data-ttu-id="29eed-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="29eed-121">Requirement</span></span> | <span data-ttu-id="29eed-122">Valore</span><span class="sxs-lookup"><span data-stu-id="29eed-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29eed-123">Versione</span><span class="sxs-lookup"><span data-stu-id="29eed-123">Version</span></span><br/> | <span data-ttu-id="29eed-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="29eed-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="29eed-125">DLL</span><span class="sxs-lookup"><span data-stu-id="29eed-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="29eed-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29eed-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29eed-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29eed-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29eed-128">**Evento Player. ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="29eed-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="29eed-129">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="29eed-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





