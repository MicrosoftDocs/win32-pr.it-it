---
description: Media streaming Terminal (MST) è un terminale dinamico basato sull'utilizzo di filtri DirectShow. Un MSP scritto usando le classi base MSP di TAPI 3 includerà un'MST, ma gli autori MSP potranno scegliere di implementarla senza usare le classi base.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Media streaming Terminal (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968908"
---
# <a name="media-streaming-terminal-mst"></a><span data-ttu-id="fde4e-104">Media streaming Terminal (MST)</span><span class="sxs-lookup"><span data-stu-id="fde4e-104">Media Streaming Terminal (MST)</span></span>

<span data-ttu-id="fde4e-105">Media streaming Terminal (MST) è un terminale dinamico basato sull'utilizzo di filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fde4e-105">The Media Streaming Terminal (MST) is a dynamic terminal based on use of DirectShow filters.</span></span> <span data-ttu-id="fde4e-106">Un MSP scritto usando le [classi base msp di TAPI 3](tapi-3-msp-base-classes.md) includerà un'MST, ma gli autori msp potranno scegliere di implementarla senza usare le classi base.</span><span class="sxs-lookup"><span data-stu-id="fde4e-106">An MSP written using the [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) will incorporate an MST, but MSP authors may choose to implement it without using the base classes.</span></span>

<span data-ttu-id="fde4e-107">Per richiamare la creazione dell'MST, un'applicazione effettua una chiamata a [**ITTerminalSupport:: CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) usando *PTERMINALCLASS* impostato su CLSID \_ MediaStreamTerminal.</span><span class="sxs-lookup"><span data-stu-id="fde4e-107">To invoke MST creation, an application makes a call to [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) using *pTerminalClass* set to CLSID\_MediaStreamTerminal.</span></span>

<span data-ttu-id="fde4e-108">Le interfacce [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) e [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) vengono quindi esposte nel terminale, consentendo a un'applicazione di ottimizzare le prestazioni di streaming.</span><span class="sxs-lookup"><span data-stu-id="fde4e-108">The [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) and [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) interfaces are then exposed on the terminal, allowing an application to tune streaming performance.</span></span> <span data-ttu-id="fde4e-109">Queste interfacce sono dichiarate in Tapi3. h.</span><span class="sxs-lookup"><span data-stu-id="fde4e-109">These interfaces are declared in Tapi3.h.</span></span>

<span data-ttu-id="fde4e-110">Per l'implementazione e l'uso di un'MST è necessaria una certa familiarità con i filtri DirectShow e la gestione dei filtri.</span><span class="sxs-lookup"><span data-stu-id="fde4e-110">Implementation and use of an MST requires familiarity with DirectShow filters and filter graph management.</span></span> <span data-ttu-id="fde4e-111">Vedere il materiale DirectShow sotto il nodo grafico e servizi multimediali della piattaforma Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fde4e-111">Please refer to the DirectShow material under the Graphic and Multimedia Services node of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="fde4e-112">Il riferimento al flusso multimediale sarà particolarmente utile per gli autori MSP.</span><span class="sxs-lookup"><span data-stu-id="fde4e-112">The Multimedia Streaming Reference will be particularly useful to MSP authors.</span></span>

 

 
