---
description: La classe di dispositivi ndis è costituita da dispositivi che possono essere associati ai driver MAC (Media Access Control) NDIS (Network Driver Interface Specification) per supportare le comunicazioni di rete. È possibile accedere a questi dispositivi usando le funzioni.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: Ndis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dda773591a3e3766a77b00925b9c15eacc5f45188900b12d6b9744c52f238ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761340"
---
# <a name="ndis"></a>Ndis

La classe di dispositivi ndis è costituita da dispositivi che possono essere associati ai driver MAC (Media Access Control) NDIS (Network Driver Interface Specification) per supportare le comunicazioni di rete. È possibile accedere a questi dispositivi usando le funzioni.

Le [**funzioni lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) riempiono una struttura [**VARSTRING,**](/windows/desktop/api/Tapi/ns-tapi-varstring) impostando il membro **dwStringFormat** sul valore STRINGFORMAT BINARY e aggiungendo \_ questi membri aggiuntivi:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

Il **membro hDevice** è l'identificatore da passare a un MAC, ad esempio il MAC asincrono per la connessione remota, per associare una connessione di rete alla connessione di chiamata/modem. Il **membro szDeviceType** è una stringa con terminazione Null che specifica il nome del dispositivo associato all'identificatore.

 

 



