---
title: Attributi direzionali applicati al parametro
description: Gli attributi direzionali \ in \ e \ out \ determinano il modo in cui il client e il server allocano e liberano memoria. Nella tabella seguente sono riepilogati gli effetti degli attributi direzionali nell'allocazione di memoria.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300250"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="30914-104">Attributi direzionali applicati al parametro</span><span class="sxs-lookup"><span data-stu-id="30914-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="30914-105">Gli attributi direzionali \[ [in](/windows/desktop/Midl/in) \] e \[ [out](/windows/desktop/Midl/out-idl) \] determinano il modo in cui il client e il server allocano e liberano memoria.</span><span class="sxs-lookup"><span data-stu-id="30914-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="30914-106">Nella tabella seguente sono riepilogati gli effetti degli attributi direzionali nell'allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="30914-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="30914-107">Attributo direzionale</span><span class="sxs-lookup"><span data-stu-id="30914-107">Directional attribute</span></span>    | <span data-ttu-id="30914-108">Memoria sul client</span><span class="sxs-lookup"><span data-stu-id="30914-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="30914-109">Memoria nel server</span><span class="sxs-lookup"><span data-stu-id="30914-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30914-110">\[[in](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="30914-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="30914-111">L'applicazione client deve allocare prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="30914-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="30914-112">Lo stub del server alloca.</span><span class="sxs-lookup"><span data-stu-id="30914-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="30914-113">\[in [uscita](/windows/desktop/Midl/out-idl)\]</span><span class="sxs-lookup"><span data-stu-id="30914-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="30914-114">Lo stub client alloca al ritorno.</span><span class="sxs-lookup"><span data-stu-id="30914-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="30914-115">Stub Server alloca solo il puntatore di primo livello. l'applicazione server deve allocare tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="30914-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="30914-116">Il server alloca inoltre i nuovi dati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="30914-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="30914-117">\[**in** **uscita**\]</span><span class="sxs-lookup"><span data-stu-id="30914-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="30914-118">L'applicazione client deve allocare i dati iniziali trasmessi al server; Stub client alloca dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="30914-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="30914-119">Stub Server alloca i dati iniziali trasmessi dal client; l'applicazione server alloca nuovi dati in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="30914-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="30914-120">In tutti questi casi lo stub del client non libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="30914-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="30914-121">L'applicazione client deve liberare la memoria prima di terminare.</span><span class="sxs-lookup"><span data-stu-id="30914-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="30914-122">Lo stub del server libera memoria quando la chiamata di procedura remota restituisce (soggetto all' \[ attributo di [allocazione](/windows/desktop/Midl/allocate) di \] ACF).</span><span class="sxs-lookup"><span data-stu-id="30914-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 