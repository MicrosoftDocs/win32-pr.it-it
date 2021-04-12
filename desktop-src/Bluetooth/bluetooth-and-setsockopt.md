---
title: Bluetooth e setsockopt
description: Bluetooth usa la funzione setsockopt per impostare vari parametri associati al canale server o alla connessione.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth e setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337751"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="13382-106">Bluetooth e setsockopt</span><span class="sxs-lookup"><span data-stu-id="13382-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="13382-107">Bluetooth usa la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per impostare vari parametri associati al canale server o alla connessione.</span><span class="sxs-lookup"><span data-stu-id="13382-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="13382-108">L'uso di **setsockopt** con Bluetooth prevede i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="13382-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="13382-109">Il parametro *s* di [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere un Socket Bluetooth valido.</span><span class="sxs-lookup"><span data-stu-id="13382-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="13382-110">Il parametro *Level* di [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve essere Sol \_ rfcomm.</span><span class="sxs-lookup"><span data-stu-id="13382-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="13382-111">Per un elenco delle opzioni dei Socket Bluetooth disponibili, vedere Opzioni per il connettore [Bluetooth e il socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="13382-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="13382-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13382-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13382-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="13382-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="13382-114">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="13382-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 