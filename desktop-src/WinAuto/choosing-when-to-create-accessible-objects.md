---
title: Scelta di quando creare oggetti accessibili
description: Gli sviluppatori di server possono creare tutti gli oggetti accessibili all'interno di un contenitore quando viene creato il contenitore oppure possono creare oggetti accessibili in modo dinamico.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045006"
---
# <a name="choosing-when-to-create-accessible-objects"></a><span data-ttu-id="b06f9-103">Scelta di quando creare oggetti accessibili</span><span class="sxs-lookup"><span data-stu-id="b06f9-103">Choosing When to Create Accessible Objects</span></span>

<span data-ttu-id="b06f9-104">Gli sviluppatori di server possono creare tutti gli oggetti accessibili all'interno di un contenitore quando viene creato il contenitore oppure possono creare oggetti accessibili in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="b06f9-104">Server developers can create all the accessible objects within a container when the container is created, or they can create the accessible objects dynamically.</span></span>

<span data-ttu-id="b06f9-105">Si supponga, ad esempio, di disporre di una finestra di dialogo con diversi controlli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b06f9-105">For example, imagine a dialog box with several custom controls.</span></span> <span data-ttu-id="b06f9-106">Un server crea oggetti accessibili per tutti i controlli personalizzati quando viene visualizzata la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b06f9-106">A server creates accessible objects for all of the custom controls when the dialog box is displayed.</span></span> <span data-ttu-id="b06f9-107">Tuttavia, se uno dei controlli è una casella combinata personalizzata, il server attende fino a quando un utente lo seleziona per creare oggetti accessibili per gli elementi contenuti nella casella combinata.</span><span class="sxs-lookup"><span data-stu-id="b06f9-107">However, if one of the controls is a custom combo box, the server waits until a user selects it to create accessible objects for the items that the combo box contains.</span></span>

<span data-ttu-id="b06f9-108">Se l'elemento padre crea oggetti accessibili in modo dinamico, le applicazioni utilizzano una quantità inferiore di memoria rispetto a quando tutti i possibili oggetti accessibili sono stati creati in anticipo.</span><span class="sxs-lookup"><span data-stu-id="b06f9-108">By having the parent create accessible objects dynamically, applications use less memory than if all the possible accessible objects were created ahead of time.</span></span>

 

 




