---
title: Funzioni di amministrazione utenti RAS
description: Usare le funzioni seguenti per gestire gli utenti di connessione remota
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473998"
---
# <a name="ras-user-administration-functions"></a><span data-ttu-id="fa865-103">Funzioni di amministrazione utenti RAS</span><span class="sxs-lookup"><span data-stu-id="fa865-103">RAS User Administration Functions</span></span>

<span data-ttu-id="fa865-104">Usare le funzioni seguenti per gestire gli utenti di connessione remota:</span><span class="sxs-lookup"><span data-stu-id="fa865-104">Use the following functions to manage dial-up users:</span></span>

-   [<span data-ttu-id="fa865-105">**MprAdminGetPDCServer**</span><span class="sxs-lookup"><span data-stu-id="fa865-105">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [<span data-ttu-id="fa865-106">**MprAdminSendUserMessage**</span><span class="sxs-lookup"><span data-stu-id="fa865-106">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [<span data-ttu-id="fa865-107">**MprAdminUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="fa865-107">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [<span data-ttu-id="fa865-108">**MprAdminUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="fa865-108">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

<span data-ttu-id="fa865-109">Per ottenere un elenco di utenti correnti in un particolare dominio, usare la funzione [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) .</span><span class="sxs-lookup"><span data-stu-id="fa865-109">To obtain a list of current users on a particular domain, use the [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) function.</span></span> <span data-ttu-id="fa865-110">Il prototipo per questa funzione si trova nel file di intestazione lmaccess. h.</span><span class="sxs-lookup"><span data-stu-id="fa865-110">The prototype for this function is in the lmaccess.h header file.</span></span>

 

 