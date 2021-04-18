---
description: La classe del dispositivo NDIS è costituita da dispositivi che possono essere associati ai driver di Network Driver Interface Specification (NDIS) Media Access Control (MAC) per supportare le comunicazioni di rete. Per accedere a questi dispositivi, è possibile usare funzioni.
ms.assetid: 98cdd929-0bd7-4509-b2f5-4edd8d6a8080
title: NDIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0be1a69f98f9a4ff8cdc2f8ea173b208c0011d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308290"
---
# <a name="ndis"></a>NDIS

La classe del dispositivo NDIS è costituita da dispositivi che possono essere associati ai driver di Network Driver Interface Specification (NDIS) Media Access Control (MAC) per supportare le comunicazioni di rete. Per accedere a questi dispositivi, è possibile usare funzioni.

Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo questi membri aggiuntivi:

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

Il membro **hDevice** è l'identificatore da passare a un Mac, ad esempio il Mac asincrono per la rete remota, per associare una connessione di rete alla connessione chiamata/modem. Il membro **szDeviceType** è una stringa con terminazione null che specifica il nome del dispositivo associato all'identificatore.

 

 



