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
# <a name="ndis"></a><span data-ttu-id="d3b11-104">NDIS</span><span class="sxs-lookup"><span data-stu-id="d3b11-104">ndis</span></span>

<span data-ttu-id="d3b11-105">La classe del dispositivo NDIS è costituita da dispositivi che possono essere associati ai driver di Network Driver Interface Specification (NDIS) Media Access Control (MAC) per supportare le comunicazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="d3b11-105">The ndis device class consists of devices that can be associated with network driver interface specification (NDIS) media access control (MAC) drivers to support network communications.</span></span> <span data-ttu-id="d3b11-106">Per accedere a questi dispositivi, è possibile usare funzioni.</span><span class="sxs-lookup"><span data-stu-id="d3b11-106">You access these devices by using functions.</span></span>

<span data-ttu-id="d3b11-107">Le funzioni [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) e [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) compilano una struttura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , impostando il membro **dwStringFormat** sul \_ valore binario STRINGFORMAT e aggiungendo questi membri aggiuntivi:</span><span class="sxs-lookup"><span data-stu-id="d3b11-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending these additional members:</span></span>

``` syntax
HANDLE  hDevice;          // NDIS connection identifier
CHAR    szDeviceType[1];  // name of device 
```

<span data-ttu-id="d3b11-108">Il membro **hDevice** è l'identificatore da passare a un Mac, ad esempio il Mac asincrono per la rete remota, per associare una connessione di rete alla connessione chiamata/modem.</span><span class="sxs-lookup"><span data-stu-id="d3b11-108">The **hDevice** member is the identifier to pass to a MAC, such as the asynchronous MAC for dial-up networking, to associate a network connection with the call/modem connection.</span></span> <span data-ttu-id="d3b11-109">Il membro **szDeviceType** è una stringa con terminazione null che specifica il nome del dispositivo associato all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="d3b11-109">The **szDeviceType** member is a null-terminated string specifying the name of the device associated with the identifier.</span></span>

 

 



