---
title: Attributo temporaneo
description: L'attributo Temporary specifica se una playlist è temporanea.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Finestra degli attributi temporanei Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325575"
---
# <a name="temporary-attribute"></a><span data-ttu-id="4dbd7-104">Attributo temporaneo</span><span class="sxs-lookup"><span data-stu-id="4dbd7-104">Temporary Attribute</span></span>

<span data-ttu-id="4dbd7-105">L'attributo **Temporary** specifica se una playlist è temporanea.</span><span class="sxs-lookup"><span data-stu-id="4dbd7-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="4dbd7-106">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="4dbd7-106">**Remarks**</span></span>

<span data-ttu-id="4dbd7-107">Se è stata recuperata una playlist dalla libreria, le modifiche apportate alla playlist verranno riflesse nella libreria dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4dbd7-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="4dbd7-108">Per evitare questo problema, chiamare [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passando il nome di attributo "Temporary" e il valore "true".</span><span class="sxs-lookup"><span data-stu-id="4dbd7-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="4dbd7-109">Questa operazione converte l'istanza della playlist in una playlist temporanea, che è sicura per la modifica senza modificare la playlist originale.</span><span class="sxs-lookup"><span data-stu-id="4dbd7-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="4dbd7-110">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="4dbd7-110">**Applies To**</span></span>

-   [<span data-ttu-id="4dbd7-111">Playlist</span><span class="sxs-lookup"><span data-stu-id="4dbd7-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="4dbd7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dbd7-112">Requirements</span></span>



| <span data-ttu-id="4dbd7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dbd7-113">Requirement</span></span> | <span data-ttu-id="4dbd7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4dbd7-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="4dbd7-115">Versione</span><span class="sxs-lookup"><span data-stu-id="4dbd7-115">Version</span></span><br/> | <span data-ttu-id="4dbd7-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="4dbd7-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4dbd7-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4dbd7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dbd7-118">**Riferimento agli attributi**</span><span class="sxs-lookup"><span data-stu-id="4dbd7-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





