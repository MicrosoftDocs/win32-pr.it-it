---
title: Handle di associazione
description: Il binding è il processo di creazione di una connessione logica tra un programma client e un programma server. Le informazioni che compongono l'associazione tra il client e il server sono rappresentate da una struttura denominata handle di associazione.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07973deb8319b44a82795a6402ef5e1a9310c2c8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516846"
---
# <a name="binding-handles"></a><span data-ttu-id="5f27c-104">Handle di associazione</span><span class="sxs-lookup"><span data-stu-id="5f27c-104">Binding Handles</span></span>

<span data-ttu-id="5f27c-105">Il binding è il processo di creazione di una connessione logica tra un programma client e un programma server.</span><span class="sxs-lookup"><span data-stu-id="5f27c-105">Binding is the process of creating a logical connection between a client program and a server program.</span></span> <span data-ttu-id="5f27c-106">Le informazioni che compongono l'associazione tra il client e il server sono rappresentate da una struttura denominata handle di associazione.</span><span class="sxs-lookup"><span data-stu-id="5f27c-106">The information that composes the binding between client and server is represented by a structure called a binding handle.</span></span>

<span data-ttu-id="5f27c-107">Un handle di associazione è analogo a un handle di file restituito dalla funzione della libreria di runtime C di FOPE o a un handle di finestra restituito dalla funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) .</span><span class="sxs-lookup"><span data-stu-id="5f27c-107">A binding handle is analogous to a file handle that the fopen C run-time library function returns, or a window handle that the function [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) returns.</span></span>

<span data-ttu-id="5f27c-108">Come con questi handle, l'applicazione non è in grado di accedere e modificare direttamente le informazioni nell'handle di binding.</span><span class="sxs-lookup"><span data-stu-id="5f27c-108">As with these handles, your application cannot directly access and manipulate the information in the binding handle.</span></span> <span data-ttu-id="5f27c-109">Le informazioni contenute in una struttura dei dati dell'handle di associazione sono disponibili solo per le librerie di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="5f27c-109">The information in a binding handle data structure is available only to the RPC run-time libraries.</span></span> <span data-ttu-id="5f27c-110">È possibile specificare l'handle, le librerie di runtime per accedere e modificare i dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="5f27c-110">You provide the handle, the run-time libraries access and manipulate the appropriate data.</span></span>

<span data-ttu-id="5f27c-111">Questa sezione presenta una discussione sugli handle di binding negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f27c-111">This section presents a discussion on binding handles in the following topics:</span></span>

-   [<span data-ttu-id="5f27c-112">Tipi di handle di associazione</span><span class="sxs-lookup"><span data-stu-id="5f27c-112">Types of Binding Handles</span></span>](types-of-binding-handles.md)
-   [<span data-ttu-id="5f27c-113">Binding lato client</span><span class="sxs-lookup"><span data-stu-id="5f27c-113">Client-Side Binding</span></span>](client-side-binding.md)
-   [<span data-ttu-id="5f27c-114">Binding lato server</span><span class="sxs-lookup"><span data-stu-id="5f27c-114">Server-Side Binding</span></span>](server-side-binding.md)
-   [<span data-ttu-id="5f27c-115">Handle con binding completo e parziale</span><span class="sxs-lookup"><span data-stu-id="5f27c-115">Fully and Partially Bound Handles</span></span>](fully-and-partially-bound-handles.md)
-   [<span data-ttu-id="5f27c-116">Interpretazione delle informazioni di binding</span><span class="sxs-lookup"><span data-stu-id="5f27c-116">Interpreting Binding Information</span></span>](interpreting-binding-information.md)
-   [<span data-ttu-id="5f27c-117">Microsoft RPC Binding-Handle Extensions</span><span class="sxs-lookup"><span data-stu-id="5f27c-117">Microsoft RPC Binding-Handle Extensions</span></span>](microsoft-rpc-binding-handle-extensions.md)
-   [<span data-ttu-id="5f27c-118">Funzioni di binding-handle</span><span class="sxs-lookup"><span data-stu-id="5f27c-118">Binding-Handle Functions</span></span>](binding-handle-functions.md)
-   [<span data-ttu-id="5f27c-119">Il database del servizio nome RPC</span><span class="sxs-lookup"><span data-stu-id="5f27c-119">The RPC Name Service Database</span></span>](the-rpc-name-service-database.md)

 

 