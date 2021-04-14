---
title: Supporto In-Process
description: L'implementazione corrente dell'annotazione dinamica è interamente in-process e di conseguenza consente solo agli elementi dell'interfaccia utente di essere annotati dal processo che possiede gli elementi dell'interfaccia utente.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328948"
---
# <a name="in-process-support"></a><span data-ttu-id="64cca-103">Supporto In-Process</span><span class="sxs-lookup"><span data-stu-id="64cca-103">In-Process Support</span></span>

<span data-ttu-id="64cca-104">L'implementazione corrente dell'annotazione dinamica è interamente in-process e di conseguenza consente solo agli elementi dell'interfaccia utente di essere annotati dal processo che possiede gli elementi dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="64cca-104">The current implementation of Dynamic Annotation is entirely in-process and consequently allows only UI elements to be annotated by the process that owns those UI elements.</span></span> <span data-ttu-id="64cca-105">Non è possibile che un processo annotare gli elementi dell'interfaccia utente di un altro processo.</span><span class="sxs-lookup"><span data-stu-id="64cca-105">It is not possible for one process to annotate the UI elements of another process.</span></span>

<span data-ttu-id="64cca-106">Si noti che questa operazione influisca solo sull'impostazione di un'annotazione. non interferisce con la capacità dei client di accedere alle proprietà (annotate o in altro modo) degli elementi dell'interfaccia utente in altri processi.</span><span class="sxs-lookup"><span data-stu-id="64cca-106">Note that this only affects the act of setting an annotation; it does not interfere with the ability of clients to access the properties (annotated or otherwise) of UI elements in other processes.</span></span>

 

 




