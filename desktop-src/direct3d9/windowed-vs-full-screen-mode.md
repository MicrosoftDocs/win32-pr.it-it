---
description: 'Le applicazioni Direct3D possono essere eseguite in una delle due modalità seguenti: schermo intero o con finestra.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modalità di confronto Full-Screen finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123849"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a><span data-ttu-id="2c9d8-103">Modalità di confronto Full-Screen finestra (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2c9d8-103">Windowed vs Full-Screen Mode (Direct3D 9)</span></span>

<span data-ttu-id="2c9d8-104">Le applicazioni Direct3D possono essere eseguite in una delle due modalità seguenti: schermo intero o con finestra.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-104">Direct3D applications can run in either of two modes: full-screen or windowed.</span></span>

<span data-ttu-id="2c9d8-105">La modalità schermo intero indica che la finestra in cui viene eseguita l'applicazione copre l'intero desktop, nascondendo tutte le applicazioni in esecuzione (incluso l'ambiente di sviluppo).</span><span class="sxs-lookup"><span data-stu-id="2c9d8-105">Full-screen mode means the window that the application runs in covers the entire desktop, hiding all running applications (including your development environment).</span></span> <span data-ttu-id="2c9d8-106">Per impostazione predefinita, i giochi usano la modalità schermo intero per immergere completamente l'utente nel gioco nascondendo tutte le applicazioni in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-106">Games typically default to full-screen mode to fully immerse the user in the game by hiding all running applications.</span></span> <span data-ttu-id="2c9d8-107">Un'applicazione in esecuzione in modalità Windows condivide il desktop con tutte le applicazioni in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-107">An application running in windowed-mode shares the desktop with all running applications.</span></span> <span data-ttu-id="2c9d8-108">Le differenze di codice tra la modalità schermo intero e la modalità finestra sono molto ridotte.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-108">Code differences between full-screen mode and windowed mode are very small.</span></span>

<span data-ttu-id="2c9d8-109">Poiché un'applicazione in esecuzione in modalità schermo intero acquisisce lo schermo, il debug dell'applicazione richiede un monitoraggio separato o l'uso di un debugger remoto.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-109">Because an application running in full-screen mode takes over the screen, debugging the application requires either a separate monitor or the use of a remote debugger.</span></span> <span data-ttu-id="2c9d8-110">Usare lo [strumento Pannello di controllo DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) per abilitare il debug di più monitor.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-110">Use the [DirectX Control Panel Tool](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) to enable multiple-monitor debugging.</span></span> <span data-ttu-id="2c9d8-111">Un vantaggio di un'applicazione in modalità finestra è che è possibile eseguire il codice un'istruzione alla volta in un debugger senza più monitoraggi o un debugger remoto.</span><span class="sxs-lookup"><span data-stu-id="2c9d8-111">One advantage of a windowed-mode application is that you can step through the code in a debugger without multiple monitors or a remote debugger.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c9d8-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c9d8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c9d8-113">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c9d8-113">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 



