---
title: La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() dalle app di Windows Store non è supportata
description: La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() dalle app di Windows Store non è supportata
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443147"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="556e6-103">La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() dalle app di Windows Store non è supportata</span><span class="sxs-lookup"><span data-stu-id="556e6-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="556e6-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="556e6-104">Platforms</span></span>

<dl> <span data-ttu-id="556e6-105">Client - Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="556e6-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="556e6-106">Servers - Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="556e6-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="556e6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="556e6-107">Description</span></span>

<span data-ttu-id="556e6-108">La chiamata di ImmSetConversionStatus() o ImmGetConversionStatus() da un'app di Windows Store non è supportata e può causare risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="556e6-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="556e6-109">Manifestazioni</span><span class="sxs-lookup"><span data-stu-id="556e6-109">Manifestations</span></span>

<span data-ttu-id="556e6-110">All'avvio dell'applicazione, la modalità IME è impostata sul valore predefinito seguente:</span><span class="sxs-lookup"><span data-stu-id="556e6-110">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="556e6-111">Pannello di input software</span><span class="sxs-lookup"><span data-stu-id="556e6-111">Software input panel</span></span> | <span data-ttu-id="556e6-112">Tastiera hardware</span><span class="sxs-lookup"><span data-stu-id="556e6-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="556e6-113">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="556e6-113">KOR, JPN</span></span> | <span data-ttu-id="556e6-114">Attivato</span><span class="sxs-lookup"><span data-stu-id="556e6-114">On</span></span>                   | <span data-ttu-id="556e6-115">Disattivato</span><span class="sxs-lookup"><span data-stu-id="556e6-115">Off</span></span>               |
| <span data-ttu-id="556e6-116">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="556e6-116">CHS, CHT</span></span> | <span data-ttu-id="556e6-117">On</span><span class="sxs-lookup"><span data-stu-id="556e6-117">On</span></span>                   | <span data-ttu-id="556e6-118">On</span><span class="sxs-lookup"><span data-stu-id="556e6-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="556e6-119">Soluzione</span><span class="sxs-lookup"><span data-stu-id="556e6-119">Solution</span></span>

<span data-ttu-id="556e6-120">Gli sviluppatori possono controllare la modalità IME predefinita specificando un valore di ambito di input per il campo.</span><span class="sxs-lookup"><span data-stu-id="556e6-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="556e6-121">La modalità IME per un ambito di input specificato è determinata da ogni IME.</span><span class="sxs-lookup"><span data-stu-id="556e6-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="556e6-122">Gli sviluppatori non possono specificare la modalità IME.</span><span class="sxs-lookup"><span data-stu-id="556e6-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="556e6-123">Risorse</span><span class="sxs-lookup"><span data-stu-id="556e6-123">Resources</span></span>

-   [<span data-ttu-id="556e6-124">Enumerazione InputScope</span><span class="sxs-lookup"><span data-stu-id="556e6-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="556e6-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="556e6-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="556e6-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="556e6-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 