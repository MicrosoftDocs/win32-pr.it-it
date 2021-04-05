---
description: Viene descritto il modo in cui l'oggetto criteri è protetto per impostazione predefinita.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protezione degli oggetti Criteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750890"
---
# <a name="policy-object-protection"></a><span data-ttu-id="281b4-103">Protezione degli oggetti Criteri</span><span class="sxs-lookup"><span data-stu-id="281b4-103">Policy Object Protection</span></span>

<span data-ttu-id="281b4-104">L'oggetto [**criteri**](policy-object.md) è protetto per impostazione predefinita con le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="281b4-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="281b4-105">Il mondo locale del gruppo dispone dell' \_ accesso Execute generico.</span><span class="sxs-lookup"><span data-stu-id="281b4-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="281b4-106">Al sistema ID noto viene concesso \_ l'accesso a tutti i criteri \_ .</span><span class="sxs-lookup"><span data-stu-id="281b4-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="281b4-107">L'amministratore locale del gruppo locale \_ dispone \_ di accesso generico Read, Generic \_ Write e Generic \_ Execute.</span><span class="sxs-lookup"><span data-stu-id="281b4-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="281b4-108">L'amministratore locale del gruppo \_ viene assegnato come proprietario e gruppo primario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="281b4-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="281b4-109">Impossibile creare o eliminare definitivamente l'oggetto [**criteri**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="281b4-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 



