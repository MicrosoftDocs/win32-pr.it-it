---
title: Aggiunta della riproduzione User-Controlled
description: Aggiunta della riproduzione User-Controlled
ms.assetid: c865bbc1-f78a-4d88-ab60-fba76818d175
keywords:
- MCIWndCreate (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 198ae0bb72a5da82042b5448d2a9213358f0174d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298259"
---
# <a name="adding-user-controlled-playback"></a><span data-ttu-id="1b01d-104">Aggiunta della riproduzione User-Controlled</span><span class="sxs-lookup"><span data-stu-id="1b01d-104">Adding User-Controlled Playback</span></span>

<span data-ttu-id="1b01d-105">È possibile aggiungere la riproduzione controllata dall'utente a un'applicazione esistente chiamando la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) come segue:</span><span class="sxs-lookup"><span data-stu-id="1b01d-105">You can add user-controlled playback to an existing application by calling the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function as follows:</span></span>


```C++
MCIWndCreate(hwndParent, hInstModule, NULL, "filename.typ"); 
```



<span data-ttu-id="1b01d-106">I parametri [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) identificano gli handle per la finestra padre e per l'istanza del modulo associata alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="1b01d-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) parameters identify handles to the parent window and to the module instance associated with the MCIWnd window.</span></span> <span data-ttu-id="1b01d-107">Specificano anche gli stili della finestra e il nome del file (o il nome del dispositivo) da associare alla finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="1b01d-107">They also specify window styles and the filename (or device name) to associate with the MCIWnd window.</span></span>

<span data-ttu-id="1b01d-108">**MCIWndCreate** esegue automaticamente i passaggi seguenti che, per le altre classi di finestra, è necessario implementare manualmente nel codice:</span><span class="sxs-lookup"><span data-stu-id="1b01d-108">**MCIWndCreate** automatically performs the following steps that, for other window classes, you would implement in your code yourself:</span></span>

1.  <span data-ttu-id="1b01d-109">Registrare la classe della finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="1b01d-109">Register the MCIWnd window class.</span></span>
2.  <span data-ttu-id="1b01d-110">Creare la finestra MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="1b01d-110">Create the MCIWnd window.</span></span>
3.  <span data-ttu-id="1b01d-111">Carica il contenuto specificato.</span><span class="sxs-lookup"><span data-stu-id="1b01d-111">Load the specified content.</span></span>
4.  <span data-ttu-id="1b01d-112">Stabilire la posizione di riproduzione corrente all'inizio del contenuto.</span><span class="sxs-lookup"><span data-stu-id="1b01d-112">Establish the current playback position at the beginning of the content.</span></span>
5.  <span data-ttu-id="1b01d-113">Visualizzare il controllo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b01d-113">Display the device control.</span></span>
6.  <span data-ttu-id="1b01d-114">Visualizzare l'area di riproduzione della finestra, se necessario.</span><span class="sxs-lookup"><span data-stu-id="1b01d-114">Display the playback area of the window, if needed.</span></span>

 

 




