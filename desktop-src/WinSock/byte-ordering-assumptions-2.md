---
description: Strutture SOCKADDR e presupposti per l'ordinamento di byte in Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Presupposti per l'ordinamento di byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307036"
---
# <a name="byte-ordering-assumptions"></a><span data-ttu-id="1632d-103">Presupposti per l'ordinamento di byte</span><span class="sxs-lookup"><span data-stu-id="1632d-103">Byte Ordering Assumptions</span></span>

<span data-ttu-id="1632d-104">Un provider di servizi deve considerare tutti i componenti [**sockaddr**](sockaddr-2.md) esclusivi del parametro della famiglia di indirizzi come se fossero nell'ordine dei byte di rete e il parametro della famiglia di indirizzi come nell'ordine dei byte del computer locale.</span><span class="sxs-lookup"><span data-stu-id="1632d-104">A service provider should treat all [**sockaddr**](sockaddr-2.md) components exclusive of the address family parameter as if they are in the network byte order, and the address family parameter as in the local computer's byte order.</span></span> <span data-ttu-id="1632d-105">È responsabilità dell'applicazione Winsock verificare che gli indirizzi contenuti nelle strutture **sockaddr** siano disposti correttamente.</span><span class="sxs-lookup"><span data-stu-id="1632d-105">It is the Winsock application's responsibility to make sure that addresses contained in **sockaddr** structures are properly arranged.</span></span> <span data-ttu-id="1632d-106">L'API Winsock fornisce diverse routine di conversione per semplificare questa attività.</span><span class="sxs-lookup"><span data-stu-id="1632d-106">The Winsock API provides a number of conversion routines to simplify this task.</span></span> <span data-ttu-id="1632d-107">Attualmente queste routine comprendono la conversione tra l'ordine dei byte naturale dell'host locale e l'ordine dei byte di rete big endian o little-endian.</span><span class="sxs-lookup"><span data-stu-id="1632d-107">Currently these routines understand conversion between the local host's natural byte order and either big-Endian or little-Endian network byte ordering.</span></span> <span data-ttu-id="1632d-108">L'architettura Winsock può supportare altri schemi di ordinamento dei byte in futuro.</span><span class="sxs-lookup"><span data-stu-id="1632d-108">The Winsock architecture can support other byte ordering schemes in the future.</span></span>

 

 



