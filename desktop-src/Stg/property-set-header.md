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
# <a name="property-set-header"></a>Intestazione set di proprietà

All'inizio del flusso di set di proprietà è presente un'intestazione. È costituito da un indicatore dell'ordine dei byte, una versione del formato, la versione del sistema operativo di origine, l'identificatore di classe (CLSID) e un campo riservato.

Nella pseudo-struttura seguente viene illustrata l'intestazione.

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

 

 




