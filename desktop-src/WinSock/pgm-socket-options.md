---
description: PGM usa le opzioni socket per impostare lo stato, fornire parametri multicast e in caso contrario implementarne le funzionalità multicast.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Opzioni socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2ec257043f86fabeafdc55ee0e7a828d495cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879189"
---
# <a name="pgm-socket-options"></a><span data-ttu-id="a5be6-103">Opzioni socket PGM</span><span class="sxs-lookup"><span data-stu-id="a5be6-103">PGM Socket Options</span></span>

<span data-ttu-id="a5be6-104">PGM usa le opzioni socket per impostare lo stato, fornire parametri multicast e in caso contrario implementarne le funzionalità multicast.</span><span class="sxs-lookup"><span data-stu-id="a5be6-104">PGM uses socket options to set state, provide multicast parameters, and otherwise implement its multicast capabilities.</span></span> <span data-ttu-id="a5be6-105">Questa pagina specifica come impostare le opzioni del socket PGM, enumera le opzioni del socket disponibili per PGM e, laddove appropriato, fornisce esempi di utilizzo e informazioni aggiuntive per le varie opzioni.</span><span class="sxs-lookup"><span data-stu-id="a5be6-105">This page specifies how PGM socket options should be set, enumerates the socket options available for PGM, and where appropriate, provides usage examples and additional information for various options.</span></span> <span data-ttu-id="a5be6-106">Per le definizioni di base di ogni opzione del socket PCM, vedere [Opzioni di socket](socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a5be6-106">For basic definitions of each PCM socket option, see [Socket Options](socket-options.md).</span></span>

<span data-ttu-id="a5be6-107">**Windows XP:** La programmazione del multicast affidabile (PGM) non è supportata.</span><span class="sxs-lookup"><span data-stu-id="a5be6-107">**Windows XP:** Reliable Multicast Programming (PGM) is not supported.</span></span>

<span data-ttu-id="a5be6-108">Per i mittenti PGM sono disponibili le seguenti opzioni di socket:</span><span class="sxs-lookup"><span data-stu-id="a5be6-108">The following socket options are available for PGM senders:</span></span>

<dl> <span data-ttu-id="a5be6-109">\_LATEJOIN RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-109">RM\_LATEJOIN</span></span>  
<span data-ttu-id="a5be6-110">\_dimensioni della \_ finestra \_ velocità RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-110">RM\_RATE\_WINDOW\_SIZE</span></span>  
<span data-ttu-id="a5be6-111">\_ \_ frequenza ADV della finestra di trasmissione RM \_ \_</span><span class="sxs-lookup"><span data-stu-id="a5be6-111">RM\_SEND\_WINDOW\_ADV\_RATE</span></span>  
<span data-ttu-id="a5be6-112">\_statistiche mittente \_ RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-112">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="a5be6-113">\_ \_ \_ Metodo Advance della finestra mittente RM \_</span><span class="sxs-lookup"><span data-stu-id="a5be6-113">RM\_SENDER\_WINDOW\_ADVANCE\_METHOD</span></span>  
<span data-ttu-id="a5be6-114">RM \_ impostare \_ mcast \_ TTL</span><span class="sxs-lookup"><span data-stu-id="a5be6-114">RM\_SET\_MCAST\_TTL</span></span>  
<span data-ttu-id="a5be6-115">\_ \_ limite messaggi set \_ RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-115">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="a5be6-116">RM \_ impostare \_ Invia \_ se</span><span class="sxs-lookup"><span data-stu-id="a5be6-116">RM\_SET\_SEND\_IF</span></span>  
<span data-ttu-id="a5be6-117">\_usare \_ FEC per RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-117">RM\_USE\_FEC</span></span>  
</dl>

<span data-ttu-id="a5be6-118">L' \_ opzione del \_ Metodo Advance della finestra mittente RM \_ \_ specifica il metodo utilizzato per l'avanzamento della finestra di invio del bordo finale.</span><span class="sxs-lookup"><span data-stu-id="a5be6-118">The RM\_SENDER\_WINDOW\_ADVANCE\_METHOD option specifies the method used when advancing the trailing edge send window.</span></span> <span data-ttu-id="a5be6-119">Il parametro optVal può essere impostato solo \_ \_ su E la finestra avanza \_ per \_ ora (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a5be6-119">The optval parameter can only be E\_WINDOW\_ADVANCE\_BY\_TIME (the default).</span></span> <span data-ttu-id="a5be6-120">Si noti che \_ l' \_ uso \_ della finestra E come \_ cache dei dati \_ non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a5be6-120">Note that E\_WINDOW\_USE\_AS\_DATA\_CACHE is not supported.</span></span>

<span data-ttu-id="a5be6-121">Per i ricevitori PGM sono disponibili le seguenti opzioni di socket:</span><span class="sxs-lookup"><span data-stu-id="a5be6-121">The following socket options are available for PGM receivers:</span></span>

<dl> <span data-ttu-id="a5be6-122">RM \_ Aggiungi \_ ricezione \_ se</span><span class="sxs-lookup"><span data-stu-id="a5be6-122">RM\_ADD\_RECEIVE\_IF</span></span>  
<span data-ttu-id="a5be6-123">RM \_ del \_ Receive \_ se</span><span class="sxs-lookup"><span data-stu-id="a5be6-123">RM\_DEL\_RECEIVE\_IF</span></span>  
<span data-ttu-id="a5be6-124">\_opt per Intranet ad alta \_ velocità \_ \_</span><span class="sxs-lookup"><span data-stu-id="a5be6-124">RM\_HIGH\_SPEED\_INTRANET\_OPT</span></span>  
<span data-ttu-id="a5be6-125">\_statistiche ricevitore \_ RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-125">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

## <a name="setting-pgm-socket-options"></a><span data-ttu-id="a5be6-126">Impostazione delle opzioni del socket PGM</span><span class="sxs-lookup"><span data-stu-id="a5be6-126">Setting PGM Socket Options</span></span>

<span data-ttu-id="a5be6-127">Il frammento di codice seguente illustra una guida di programmazione per l'impostazione delle opzioni del socket PGM:</span><span class="sxs-lookup"><span data-stu-id="a5be6-127">The following code snippet illustrates a programming guideline for setting PGM socket options:</span></span>


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



<span data-ttu-id="a5be6-128">Nel frammento di codice precedente, il tipo e il contenuto di *OptionData* dipendono dall'opzione socket da impostare.</span><span class="sxs-lookup"><span data-stu-id="a5be6-128">In the snippet above, the type and contents of *OptionData* are dependent on the socket option being set.</span></span> <span data-ttu-id="a5be6-129">Per tutte le opzioni del socket PGM, il livello di socket è IPPROTO \_ RM.</span><span class="sxs-lookup"><span data-stu-id="a5be6-129">For all PGM socket options, the socket level is IPPROTO\_RM.</span></span> <span data-ttu-id="a5be6-130">È necessario impostare le opzioni del socket PGM immediatamente dopo la chiamata alla funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , con le eccezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a5be6-130">PGM socket options must be set immediately following the call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, with the following exceptions:</span></span>

<dl> <span data-ttu-id="a5be6-131">\_ \_ limite messaggi set \_ RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-131">RM\_SET\_MESSAGE\_BOUNDARY</span></span>  
<span data-ttu-id="a5be6-132">\_statistiche mittente \_ RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-132">RM\_SENDER\_STATISTICS</span></span>  
<span data-ttu-id="a5be6-133">\_statistiche ricevitore \_ RM</span><span class="sxs-lookup"><span data-stu-id="a5be6-133">RM\_RECEIVER\_STATISTICS</span></span>  
</dl>

 

 



