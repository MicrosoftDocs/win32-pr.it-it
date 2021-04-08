---
title: Bluetooth e getsockopt
description: Bluetooth usa la funzione getsockopt per eseguire una query sui diversi parametri associati al canale server o alla connessione.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth e getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728362"
---
# <a name="bluetooth-and-getsockopt"></a><span data-ttu-id="12339-106">Bluetooth e getsockopt</span><span class="sxs-lookup"><span data-stu-id="12339-106">Bluetooth and getsockopt</span></span>

<span data-ttu-id="12339-107">Bluetooth usa la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per eseguire una query sui diversi parametri associati al canale server o alla connessione.</span><span class="sxs-lookup"><span data-stu-id="12339-107">Bluetooth uses the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function to query various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="12339-108">L'uso di **getsockopt** con Bluetooth prevede i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="12339-108">Use of **getsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="12339-109">Il parametro *s* di [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve essere un Socket Bluetooth valido.</span><span class="sxs-lookup"><span data-stu-id="12339-109">The *s* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="12339-110">Il parametro *Level* di [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve essere Sol \_ rfcomm.</span><span class="sxs-lookup"><span data-stu-id="12339-110">The *level* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="12339-111">Per un elenco delle opzioni dei Socket Bluetooth disponibili, vedere Opzioni per il connettore [Bluetooth e il socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="12339-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12339-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12339-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12339-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="12339-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="12339-114">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="12339-114">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 