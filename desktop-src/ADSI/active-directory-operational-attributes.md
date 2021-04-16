---
title: Active Directory gli attributi operativi
description: Gli attributi operativi sono proprietà archiviate e utilizzate dalla directory per scopi amministrativi.
ms.assetid: 07453dc0-747e-4b34-946e-1adb90ea532c
ms.tgt_platform: multiple
keywords:
- attributi ADSI, attributi operativi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95536564f735e8e1bd8c5c28a49ce71a2640a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395314"
---
# <a name="active-directory-operational-attributes"></a><span data-ttu-id="56ede-104">Active Directory gli attributi operativi</span><span class="sxs-lookup"><span data-stu-id="56ede-104">Active Directory Operational Attributes</span></span>

<span data-ttu-id="56ede-105">Gli attributi operativi sono proprietà archiviate e utilizzate dalla directory per scopi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="56ede-105">Operational attributes are properties that are stored in and used by the directory for administrative purposes.</span></span> <span data-ttu-id="56ede-106">Ad esempio, è possibile mantenere un attributo operativo per registrare la data e l'ora di modifica di un altro attributo.</span><span class="sxs-lookup"><span data-stu-id="56ede-106">For example, you might maintain an operational attribute to log the date and time when another attribute is modified.</span></span> <span data-ttu-id="56ede-107">Gli attributi operativi devono essere recuperati in modo esplicito con una chiamata a [**GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex).</span><span class="sxs-lookup"><span data-stu-id="56ede-107">Operational Attributes must be explicitly retrieved with a call to [**GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex).</span></span>

 

 




