---
description: ATM è applicabile agli ambienti LAN e WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Allegato ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308864"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="01fe8-103">Allegato ATM Winsock</span><span class="sxs-lookup"><span data-stu-id="01fe8-103">Winsock ATM Annex</span></span>

<span data-ttu-id="01fe8-104">ATM è applicabile agli ambienti LAN e WAN.</span><span class="sxs-lookup"><span data-stu-id="01fe8-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="01fe8-105">Una rete ATM trasporta simultaneamente un'ampia gamma di traffico di rete: voce, dati, immagine e video.</span><span class="sxs-lookup"><span data-stu-id="01fe8-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="01fe8-106">Fornisce agli utenti una qualità del servizio garantita in base a un canale virtuale (VC).</span><span class="sxs-lookup"><span data-stu-id="01fe8-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="01fe8-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="01fe8-107">Element</span></span>          | <span data-ttu-id="01fe8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01fe8-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01fe8-109">Nome/i protocollo</span><span class="sxs-lookup"><span data-stu-id="01fe8-109">Protocol name(s)</span></span> | <span data-ttu-id="01fe8-110">ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER</span><span class="sxs-lookup"><span data-stu-id="01fe8-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="01fe8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01fe8-111">Description</span></span>      | <span data-ttu-id="01fe8-112">AAL5 ATM fornisce un servizio di trasporto che è orientato alla connessione, mantenuto al limite dei messaggi e garantito QOS.</span><span class="sxs-lookup"><span data-stu-id="01fe8-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="01fe8-113">ATMPROTO \_ AALUSER è un Aal definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="01fe8-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="01fe8-114">Famiglia di indirizzi</span><span class="sxs-lookup"><span data-stu-id="01fe8-114">Address family</span></span>   | <span data-ttu-id="01fe8-115">\_ATM AF</span><span class="sxs-lookup"><span data-stu-id="01fe8-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="01fe8-116">File di intestazione</span><span class="sxs-lookup"><span data-stu-id="01fe8-116">Header file</span></span>      | <span data-ttu-id="01fe8-117">Ws2atm. h</span><span class="sxs-lookup"><span data-stu-id="01fe8-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="01fe8-118">In questa sezione vengono descritte le estensioni specifiche di ATM (Asynchronous Transfer Mode) necessarie per supportare i servizi ATM nativi come esposti e specificati nella specifica della versione 3. x (3,0 e 3,1) di ATM Forum User Network Interface (UNI).</span><span class="sxs-lookup"><span data-stu-id="01fe8-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="01fe8-119">Questo documento supporta AAL di tipo 5 (modalità messaggio) e AAL definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="01fe8-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="01fe8-120">Le versioni future di questo documento supporteranno altri tipi di AAL, nonché UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="01fe8-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



