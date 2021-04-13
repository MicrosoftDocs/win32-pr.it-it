---
description: Il monitoraggio di rete chiama la funzione RecognizeFrame di un parser per determinare che il parser riconosce i dati non reclamati di un frame.
ms.assetid: 6d0574da-f0ec-4ed9-bfb0-023dff2ac6fe
title: Implementazione di RecognizeFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d970eee80a04168b3fa06b117c2c219c506da7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348946"
---
# <a name="implementing-recognizeframe"></a><span data-ttu-id="3d615-103">Implementazione di RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="3d615-103">Implementing RecognizeFrame</span></span>

<span data-ttu-id="3d615-104">Il monitoraggio di rete chiama la funzione [**RecognizeFrame**](recognizeframe.md) di un parser per determinare che il parser riconosce i dati non reclamati di un frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-104">Network Monitors calls the [**RecognizeFrame**](recognizeframe.md) function of a parser to determine that the parser recognizes the unclaimed data of a frame.</span></span> <span data-ttu-id="3d615-105">I dati non reclamati potrebbero essere all'inizio di un frame, ma in genere i dati non reclamati si trovano al centro di un frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-105">The unclaimed data may be at the start of a frame, but typically, unclaimed data is located in the middle of a frame.</span></span> <span data-ttu-id="3d615-106">Nella figura seguente vengono mostrati i dati non recuperati che si trovano al centro di un frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-106">The following illustration shows unclaimed data located in the middle of a frame.</span></span>

![dati non reclamati che si trovano al centro di un frame](images/recognizeframe1.png)

<span data-ttu-id="3d615-108">Network Monitor fornisce le informazioni seguenti quando chiama la funzione [**RecognizeFrame**](recognizeframe.md) :</span><span class="sxs-lookup"><span data-stu-id="3d615-108">Network Monitor provides the following information when it calls the [**RecognizeFrame**](recognizeframe.md) function:</span></span>

-   <span data-ttu-id="3d615-109">Handle per il frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-109">A handle to the frame.</span></span>
-   <span data-ttu-id="3d615-110">Puntatore all'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-110">A pointer to the start of the frame.</span></span>
-   <span data-ttu-id="3d615-111">Puntatore all'inizio dei dati non recuperati.</span><span class="sxs-lookup"><span data-stu-id="3d615-111">A pointer to the start of the unclaimed data.</span></span>
-   <span data-ttu-id="3d615-112">Valore MAC del primo protocollo nel frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-112">The MAC value of the first protocol in the frame.</span></span>
-   <span data-ttu-id="3d615-113">Numero di byte nei dati non recuperati; ovvero i byte rimanenti nel frame.</span><span class="sxs-lookup"><span data-stu-id="3d615-113">The number of bytes in the unclaimed data; that is, the bytes remaining in the frame.</span></span>
-   <span data-ttu-id="3d615-114">Handle per il protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="3d615-114">A handle to the previous protocol.</span></span>
-   <span data-ttu-id="3d615-115">Offset del protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="3d615-115">The offset of the previous protocol.</span></span>

<span data-ttu-id="3d615-116">Quando la DLL del parser determina che i dati non reclamati iniziano con il protocollo del parser, la DLL del parser determina la posizione in cui inizia il protocollo successivo e il protocollo che segue.</span><span class="sxs-lookup"><span data-stu-id="3d615-116">When the parser DLL determines that unclaimed data starts with the parser protocol, the parser DLL determines where the next protocol starts, and which protocol follows.</span></span> <span data-ttu-id="3d615-117">La DLL del parser funziona nei modi condizionali seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d615-117">The parser DLL functions in the following conditional ways:</span></span>

-   <span data-ttu-id="3d615-118">Se la DLL del parser riconosce i dati non recuperati, la DLL del parser imposta il parametro *pProtocolStatus* e restituisce un puntatore al protocollo successivo nel frame o **null**.</span><span class="sxs-lookup"><span data-stu-id="3d615-118">If the parser DLL recognizes unclaimed data, the parser DLL sets the *pProtocolStatus* parameter, and returns a pointer to either the next protocol in the frame, or **NULL**.</span></span> <span data-ttu-id="3d615-119">Se il protocollo corrente è l'ultimo protocollo nel frame, viene restituito **null** .</span><span class="sxs-lookup"><span data-stu-id="3d615-119">**NULL** is returned if the current protocol is the last protocol in the frame.</span></span>
-   <span data-ttu-id="3d615-120">Se la DLL del parser riconosce i dati non attestati e identifica il protocollo che segue (dalle informazioni fornite nel protocollo), la DLL del parser restituisce un puntatore all'handle del protocollo successivo nel parametro *phNextProtocol* della funzione.</span><span class="sxs-lookup"><span data-stu-id="3d615-120">If the parser DLL recognizes unclaimed data and identifies the protocol that follows (from information provided in the protocol), then the parser DLL returns a pointer to the handle of the next protocol in the *phNextProtocol* parameter of the function.</span></span>
-   <span data-ttu-id="3d615-121">Se la DLL del parser non riconosce i dati non reclamati, la DLL del parser restituisce il puntatore all'inizio dei dati non attestati e Network Monitor continua a provare ad analizzare i dati non recuperati.</span><span class="sxs-lookup"><span data-stu-id="3d615-121">If the parser DLL does not recognize unclaimed data, the parser DLL returns the pointer to the start of unclaimed data, and Network Monitor continues trying to parse the unclaimed data.</span></span>

<span data-ttu-id="3d615-122">**Per implementare RecognizeFrame**</span><span class="sxs-lookup"><span data-stu-id="3d615-122">**To implement RecognizeFrame**</span></span>

1.  <span data-ttu-id="3d615-123">Eseguire un test per determinare se il protocollo è riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3d615-123">Test to determine that you recognize the protocol.</span></span>
2.  <span data-ttu-id="3d615-124">Se si riconoscono i dati non reclamati e si sa quale protocollo segue, impostare *pProtocolStatus* su protocollo \_ status \_ Next \_ Protocol, impostare *phNextProtocol* su un puntatore che punta all'handle per il protocollo successivo, quindi restituire un puntatore al protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="3d615-124">If you recognize unclaimed data and you know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_NEXT\_PROTOCOL, set *phNextProtocol* to a pointer that points to the handle for the next protocol, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="3d615-125">–oppure–</span><span class="sxs-lookup"><span data-stu-id="3d615-125">–or–</span></span>

    <span data-ttu-id="3d615-126">Se si riconoscono i dati non reclamati e non si sa quale protocollo segue  , impostare pProtocolStatus \_ sullo stato \_ del protocollo riconosciuto e quindi restituire un puntatore al protocollo successivo.</span><span class="sxs-lookup"><span data-stu-id="3d615-126">If you recognize unclaimed data and you do not know which protocol follows, set *pProtocolStatus* to PROTOCOL\_STATUS\_RECOGNIZED, and then return a pointer to the next protocol.</span></span>

    <span data-ttu-id="3d615-127">–oppure–</span><span class="sxs-lookup"><span data-stu-id="3d615-127">–or–</span></span>

    <span data-ttu-id="3d615-128">Se si riconoscono i dati non richiesti e il protocollo è l'ultimo protocollo in un frame  , impostare pProtocolStatus \_ sullo stato del protocollo \_ richiesto e quindi restituire **null**.</span><span class="sxs-lookup"><span data-stu-id="3d615-128">If you recognize unclaimed data and your protocol is the last protocol in a frame, set *pProtocolStatus* to PROTOCOL\_STATUS\_CLAIMED, and then return **NULL**.</span></span>

    <span data-ttu-id="3d615-129">–oppure–</span><span class="sxs-lookup"><span data-stu-id="3d615-129">–or–</span></span>

    <span data-ttu-id="3d615-130">Se non si riconoscono i dati non attestati  , impostare pProtocolStatus \_ sullo stato \_ del protocollo non \_ riconosciuto, quindi restituire il puntatore passato all'utente in *pProtocol*.</span><span class="sxs-lookup"><span data-stu-id="3d615-130">If you do not recognize unclaimed data, set *pProtocolStatus* to PROTOCOL\_STATUS\_NOT\_RECOGNIZED, and then return the pointer that is passed to you in *pProtocol*.</span></span>

<span data-ttu-id="3d615-131">Di seguito è riportata un'implementazione di base di [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="3d615-131">The following is a basic implementation of [**RecognizeFrame**](recognizeframe.md).</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocol_RecognizeFrame( HFRAME hFrame,
                                        LPBYTE        pMacFrame,
                                        LPBYTE        pProtocol,
                                        DWORD         MacType,
                                        DWORD         BytesLeft,
                                        HPROTOCOL     hPrevProtocol,
                                        DWORD         nPreviuosProtOffset,
                                        LPDWORD       pProtocolStatus,
                                        LPHPROTOCOL   phNextProtocol,
                                        LPDWORD       InstData)
  
  // Test unclaimed data. 
  
  // If unclaimed data is recognized, but you do not know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_RECOGNIZED;
  return pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and you know what follows.
  *pProtocolStatus =  PROTOCOL_STATUS_NEXT_PROTOCOL;
  phNextProtocol = GetProtocolFromTable(
                                        hTable,
                                        ItemToFind,
                                        lpInstData);
  return  pProtocol + MY_PROTOCOL_LENGTH;
  
  // If unclaimed data is recognized and the protocol is the last 
  // protocol in the frame.
  *pProtocolStatus =  PROTOCOL_STATUS_CLAIMED;
  return NULL;
  
  // If the unclaimed data is not recognized.
  *pProtocolStatus =  PROTOCOL_STATUS_NOT_RECOGNIZED;
  return *pProtocol;

}
```

 

 



