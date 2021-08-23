---
title: Intestazione del set di proprietà
description: All'inizio del flusso del set di proprietà è un'intestazione. È costituito da un indicatore dell'ordine dei byte, una versione del formato, la versione del sistema operativo di origine, l'identificatore di classe (CLSID) e un campo riservato.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Intestazione del set di proprietà strutturata Archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662221"
---
# <a name="property-set-header"></a>Intestazione del set di proprietà

All'inizio del flusso del set di proprietà è un'intestazione. È costituito da un indicatore dell'ordine dei byte, una versione del formato, la versione del sistema operativo di origine, l'identificatore di classe (CLSID) e un campo riservato.

La pseudo-struttura seguente illustra l'intestazione.

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

 

 




