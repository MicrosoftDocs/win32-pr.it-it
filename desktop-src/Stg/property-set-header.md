---
title: Intestazione set di proprietà
description: All'inizio del flusso di set di proprietà è presente un'intestazione. È costituito da un indicatore dell'ordine dei byte, una versione del formato, la versione del sistema operativo di origine, l'identificatore di classe (CLSID) e un campo riservato.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Archiviazione strutturata intestazione set di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332727"
---
# <a name="property-set-header"></a><span data-ttu-id="455ab-105">Intestazione set di proprietà</span><span class="sxs-lookup"><span data-stu-id="455ab-105">Property Set Header</span></span>

<span data-ttu-id="455ab-106">All'inizio del flusso di set di proprietà è presente un'intestazione.</span><span class="sxs-lookup"><span data-stu-id="455ab-106">At the beginning of the property set stream is a header.</span></span> <span data-ttu-id="455ab-107">È costituito da un indicatore dell'ordine dei byte, una versione del formato, la versione del sistema operativo di origine, l'identificatore di classe (CLSID) e un campo riservato.</span><span class="sxs-lookup"><span data-stu-id="455ab-107">It consists of a byte-order indicator, a format version, the originating operating system version, the class identifier (CLSID), and a reserved field.</span></span>

<span data-ttu-id="455ab-108">Nella pseudo-struttura seguente viene illustrata l'intestazione.</span><span class="sxs-lookup"><span data-stu-id="455ab-108">The following pseudo-structure illustrates the header.</span></span>

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




