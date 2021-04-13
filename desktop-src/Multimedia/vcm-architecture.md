---
title: Architettura VCM
description: Architettura VCM
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video per Windows (VFW), architettura VCM
- VFW (video per Windows), architettura VCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331055"
---
# <a name="vcm-architecture"></a><span data-ttu-id="92136-105">Architettura VCM</span><span class="sxs-lookup"><span data-stu-id="92136-105">VCM Architecture</span></span>

<span data-ttu-id="92136-106">VCM è un intermediario tra un'applicazione e i driver di compressione e decompressione.</span><span class="sxs-lookup"><span data-stu-id="92136-106">VCM is an intermediary between an application and compression and decompression drivers.</span></span> <span data-ttu-id="92136-107">I driver di compressione e decompressione comprimeno e decomprimeno singoli frame di dati.</span><span class="sxs-lookup"><span data-stu-id="92136-107">The compression and decompression drivers compress and decompress individual frames of data.</span></span>

<span data-ttu-id="92136-108">Quando un'applicazione effettua una chiamata a VCM, VCM converte la chiamata in un messaggio.</span><span class="sxs-lookup"><span data-stu-id="92136-108">When an application makes a call to VCM, VCM translates the call into a message.</span></span> <span data-ttu-id="92136-109">Il messaggio viene inviato tramite la funzione [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) al commediatore o al decompressore appropriato, che comprime o decomprime i dati.</span><span class="sxs-lookup"><span data-stu-id="92136-109">The message is sent by using the [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) function to the appropriate compressor or decompressor, which compresses or decompresses the data.</span></span> <span data-ttu-id="92136-110">VCM riceve il valore restituito dal driver di compressione o decompressione e quindi restituisce il controllo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="92136-110">VCM receives the return value from the compression or decompression driver and then returns control to the application.</span></span>

<span data-ttu-id="92136-111">Se una macro viene definita per un messaggio, la macro si espande in una chiamata di funzione **ICSendMessage** che fornisce parametri appropriati per il messaggio.</span><span class="sxs-lookup"><span data-stu-id="92136-111">If a macro is defined for a message, the macro expands to an **ICSendMessage** function call supplying appropriate parameters for that message.</span></span> <span data-ttu-id="92136-112">Se viene definita una macro per un messaggio, l'applicazione deve utilizzarla anziché il messaggio.</span><span class="sxs-lookup"><span data-stu-id="92136-112">If a macro is defined for a message, your application should use it rather than the message.</span></span> <span data-ttu-id="92136-113">In questa panoramica queste macro seguono i messaggi tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="92136-113">In this overview, these macros follow messages in parentheses.</span></span>

 

 




