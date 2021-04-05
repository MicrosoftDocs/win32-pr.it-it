---
title: La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata
description: La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727695"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="6edf2-103">La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () dalle app di Windows Store non è supportata</span><span class="sxs-lookup"><span data-stu-id="6edf2-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="6edf2-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="6edf2-104">Platforms</span></span>

<dl> <span data-ttu-id="6edf2-105">Client-Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="6edf2-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="6edf2-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6edf2-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="6edf2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6edf2-107">Description</span></span>

<span data-ttu-id="6edf2-108">La chiamata a ImmSetConversionStatus () o ImmGetConversionStatus () da un'app di Windows Store non è supportata e può causare risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="6edf2-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="6edf2-109">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="6edf2-109">Manifestations</span></span>

<span data-ttu-id="6edf2-110">All'avvio dell'applicazione, la modalità IME è impostata sui valori predefiniti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6edf2-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="6edf2-111">Pannello di input software</span><span class="sxs-lookup"><span data-stu-id="6edf2-111">Software input panel</span></span> | <span data-ttu-id="6edf2-112">Tastiera hardware</span><span class="sxs-lookup"><span data-stu-id="6edf2-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="6edf2-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="6edf2-113">KOR, JPN</span></span> | <span data-ttu-id="6edf2-114">Attivato</span><span class="sxs-lookup"><span data-stu-id="6edf2-114">On</span></span>                   | <span data-ttu-id="6edf2-115">Disattivato</span><span class="sxs-lookup"><span data-stu-id="6edf2-115">Off</span></span>               |
| <span data-ttu-id="6edf2-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="6edf2-116">CHS, CHT</span></span> | <span data-ttu-id="6edf2-117">Attivato</span><span class="sxs-lookup"><span data-stu-id="6edf2-117">On</span></span>                   | <span data-ttu-id="6edf2-118">Attivato</span><span class="sxs-lookup"><span data-stu-id="6edf2-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="6edf2-119">Soluzione</span><span class="sxs-lookup"><span data-stu-id="6edf2-119">Solution</span></span>

<span data-ttu-id="6edf2-120">Gli sviluppatori possono controllare la modalità IME predefinita specificando un valore dell'ambito di input per il campo.</span><span class="sxs-lookup"><span data-stu-id="6edf2-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="6edf2-121">La modalità IME per un ambito di input specificato è determinata da ogni IME.</span><span class="sxs-lookup"><span data-stu-id="6edf2-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="6edf2-122">Gli sviluppatori non possono specificare la modalità IME.</span><span class="sxs-lookup"><span data-stu-id="6edf2-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="6edf2-123">Risorse</span><span class="sxs-lookup"><span data-stu-id="6edf2-123">Resources</span></span>

-   [<span data-ttu-id="6edf2-124">Enumerazione InputScope</span><span class="sxs-lookup"><span data-stu-id="6edf2-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="6edf2-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="6edf2-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="6edf2-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="6edf2-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 