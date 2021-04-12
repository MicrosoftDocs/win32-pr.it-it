---
title: Preparazione dell'applicazione per Windows a 64 bit
description: Sono disponibili diverse funzionalità che semplificano lo sviluppo di applicazioni che verranno eseguite su Windows a 32 e 64 bit. La maggior parte di questi, ad esempio i nuovi tipi di dati, è descritta in preparazione per Windows a 64 bit.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Programmazione Windows a 64 bit Toolkit a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104224004"
---
# <a name="preparing-your-application-for-64-bit-windows"></a><span data-ttu-id="46648-105">Preparazione dell'applicazione per Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="46648-105">Preparing Your Application for 64-bit Windows</span></span>

<span data-ttu-id="46648-106">Sono disponibili diverse funzionalità che semplificano lo sviluppo di applicazioni che verranno eseguite su Windows a 32 e 64 bit.</span><span class="sxs-lookup"><span data-stu-id="46648-106">There are several features that make it easier for you to develop applications that will run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="46648-107">La maggior parte di questi, ad esempio i nuovi tipi di dati, è descritta in [preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="46648-107">Most of these, such as the new data types, are described in [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

<span data-ttu-id="46648-108">Il Toolkit a 64 bit fornito con la Windows SDK include un compilatore MIDL a 64 bit, Midl.exe, per la generazione di stub a 64 bit nativi, oltre a Stub a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="46648-108">The 64-bit toolkit that ships with the Windows SDK includes a 64-bit MIDL compiler, Midl.exe, for generating native 64-bit stubs, as well as 32-bit stubs.</span></span> <span data-ttu-id="46648-109">Usare l'opzione **/ENV Win64** per generare solo stub a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="46648-109">Use the **/env win64** switch to generate 64-bit stubs only.</span></span> <span data-ttu-id="46648-110">Per impostazione predefinita, vengono generati doppi Stub eseguiti su entrambe le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="46648-110">The default is to generate dual stubs that run on both platforms.</span></span>

<span data-ttu-id="46648-111">Si noti che MIDL a 64 bit supporta solo le modalità di ottimizzazione [**/Oicf**](/windows/desktop/Midl/-oi) e [**/OS**](/windows/desktop/Midl/-os) .</span><span class="sxs-lookup"><span data-stu-id="46648-111">Note that the 64-bit MIDL supports the [**/Oicf**](/windows/desktop/Midl/-oi) and [**/Os**](/windows/desktop/Midl/-os) optimization modes only.</span></span>

 

 