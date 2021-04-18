---
title: Struttura RAS_PORT_STATISTICS (rassapi. h)
description: La \_ struttura delle statistiche della porta RAS \_ riporta le statistiche che un server RAS raccoglie per una porta connessa.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS struttura RAS_PORT_STATISTICS
- RAS puntatore alla struttura PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301754"
---
# <a name="ras_port_statistics-structure"></a><span data-ttu-id="79e28-105">Struttura delle statistiche della \_ porta RAS \_</span><span class="sxs-lookup"><span data-stu-id="79e28-105">RAS\_PORT\_STATISTICS structure</span></span>

<span data-ttu-id="79e28-106">\[La struttura delle **\_ \_ statistiche della porta RAS** non è supportata a partire da Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="79e28-106">\[The **RAS\_PORT\_STATISTICS** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="79e28-107">La struttura delle **\_ \_ statistiche della porta RAS** riporta le statistiche che un server RAS raccoglie per una porta connessa.</span><span class="sxs-lookup"><span data-stu-id="79e28-107">The **RAS\_PORT\_STATISTICS** structure reports the statistics that a RAS server collects for a connected port.</span></span> <span data-ttu-id="79e28-108">Il server RAS Reimposta i vari contatori statistici ogni volta che la porta è connessa.</span><span class="sxs-lookup"><span data-stu-id="79e28-108">The RAS server resets the various statistic counters each time the port is connected.</span></span> <span data-ttu-id="79e28-109">Chiamare la funzione [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) per forzare la reimpostazione dei contatori delle statistiche da parte del server RAS.</span><span class="sxs-lookup"><span data-stu-id="79e28-109">Call the [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) function to force the RAS server to reset the statistic counters.</span></span>

<span data-ttu-id="79e28-110">Per una porta che fa parte di una connessione a più collegamenti, questa struttura fornisce due set di statistiche.</span><span class="sxs-lookup"><span data-stu-id="79e28-110">For a port that is part of a multilink connection, this structure provides two sets of statistics.</span></span> <span data-ttu-id="79e28-111">Il primo set contiene le statistiche cumulative per tutte le porte della connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-111">The first set contains the cumulative statistics for all ports in the connection.</span></span> <span data-ttu-id="79e28-112">Queste statistiche sono le stesse per tutte le porte della connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-112">These statistics are the same for all ports in the connection.</span></span> <span data-ttu-id="79e28-113">Il secondo set contiene le statistiche solo per questa porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-113">The second set contains the statistics for just this port.</span></span> <span data-ttu-id="79e28-114">Se la porta non fa parte di una connessione a più collegamenti, entrambi i set di statistiche avranno le stesse informazioni.</span><span class="sxs-lookup"><span data-stu-id="79e28-114">If the port is not part of a multilink connection, both sets of statistics have the same information.</span></span> <span data-ttu-id="79e28-115">Per determinare se una porta fa parte di una connessione a più collegamenti, controllare il \_ bit a collegamento multiplo della porta nel membro **flag** della struttura [**della \_ porta di Ras \_ 0**](ras-port-0-str.md) della porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-115">To determine whether a port is part of a multilink connection, check the PORT\_MULTILINKED bit in the **Flags** member of the port's [**RAS\_PORT\_0**](ras-port-0-str.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e28-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79e28-116">Syntax</span></span>


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a><span data-ttu-id="79e28-117">Members</span><span class="sxs-lookup"><span data-stu-id="79e28-117">Members</span></span>

<dl> <dt>

<span data-ttu-id="79e28-118">**dwBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="79e28-118">**dwBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-119">Specifica il numero totale di byte trasmessi dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-119">Specifies the total number of bytes transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-120">**dwBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="79e28-120">**dwBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-121">Specifica il numero totale di byte ricevuti dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-121">Specifies the total number of bytes received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-122">**dwFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="79e28-122">**dwFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-123">Specifica il numero totale di frame trasmessi dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-123">Specifies the total number of frames transmitted by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-124">**dwFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="79e28-124">**dwFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-125">Specifica il numero totale di frame ricevuti dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-125">Specifies the total number of frames received by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-126">**dwCrcErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-126">**dwCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-127">Specifica il numero totale di errori CRC sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-127">Specifies the total number of CRC errors on the connection.</span></span> <span data-ttu-id="79e28-128">Gli errori CRC sono causati dall'esito negativo di un controllo di ridondanza ciclico.</span><span class="sxs-lookup"><span data-stu-id="79e28-128">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="79e28-129">Un errore CRC indica che uno o più caratteri nel pacchetto di dati ricevuti sono stati rilevati all'arrivo.</span><span class="sxs-lookup"><span data-stu-id="79e28-129">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-130">**dwTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-130">**dwTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-131">Specifica il numero totale di errori di timeout della connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-131">Specifies the total number of time-out errors on the connection.</span></span> <span data-ttu-id="79e28-132">Gli errori di timeout si verificano quando un carattere previsto non viene ricevuto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="79e28-132">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="79e28-133">Quando si verifica questo problema, il software presuppone che i dati siano andati perduti e che ne richieda il reinviato.</span><span class="sxs-lookup"><span data-stu-id="79e28-133">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-134">**dwAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-134">**dwAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-135">Specifica il numero totale di errori di allineamento nella connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-135">Specifies the total number of alignment errors on the connection.</span></span> <span data-ttu-id="79e28-136">Gli errori di allineamento si verificano quando un carattere ricevuto non è quello previsto.</span><span class="sxs-lookup"><span data-stu-id="79e28-136">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="79e28-137">Questa situazione si verifica in genere quando un carattere viene perso o si verifica un errore di timeout.</span><span class="sxs-lookup"><span data-stu-id="79e28-137">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-138">**dwHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-138">**dwHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-139">Specifica il numero totale di errori di sovraccarico hardware sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-139">Specifies the total number of hardware overrun errors on the connection.</span></span> <span data-ttu-id="79e28-140">Questi errori indicano il numero di volte in cui il computer di invio ha trasmesso i caratteri più velocemente di quanto l'hardware del computer ricevente possa elaborarli.</span><span class="sxs-lookup"><span data-stu-id="79e28-140">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="79e28-141">Se il problema persiste, ridurre la velocità di connessione BPS nel client.</span><span class="sxs-lookup"><span data-stu-id="79e28-141">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-142">**dwFramingErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-142">**dwFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-143">Specifica il numero totale di errori di frame sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-143">Specifies the total number of framing errors on the connection.</span></span> <span data-ttu-id="79e28-144">Un errore di framing si verifica quando viene ricevuto un carattere asincrono con un bit di avvio o di arresto non valido.</span><span class="sxs-lookup"><span data-stu-id="79e28-144">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-145">**dwBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-145">**dwBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-146">Specifica il numero totale di errori di sovraccarico del buffer nella connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-146">Specifies the total number of buffer overrun errors on the connection.</span></span> <span data-ttu-id="79e28-147">Si verifica un errore di sovraccarico del buffer quando il computer mittente trasmette caratteri più velocemente di quanto il computer ricevente possa adattarlo.</span><span class="sxs-lookup"><span data-stu-id="79e28-147">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="79e28-148">Se il problema persiste, ridurre la velocità di connessione BPS nel client.</span><span class="sxs-lookup"><span data-stu-id="79e28-148">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-149">**dwBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-149">**dwBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-150">Specifica il numero totale di byte trasmessi non compressi dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-150">Specifies the total number of bytes transmitted uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-151">**dwBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-151">**dwBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-152">Specifica il numero totale di byte ricevuti decompressi dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-152">Specifies the total number of bytes received uncompressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-153">**dwBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-153">**dwBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-154">Specifica il numero totale di byte trasmessi dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-154">Specifies the total number of bytes transmitted compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-155">**dwBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-155">**dwBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-156">Specifica il numero totale di byte ricevuti compressi dalla connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-156">Specifies the total number of bytes received compressed by the connection.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-157">**dwPortBytesXmited**</span><span class="sxs-lookup"><span data-stu-id="79e28-157">**dwPortBytesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-158">Specifica il numero totale di byte trasmessi dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-158">Specifies the total number of bytes transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-159">**dwPortBytesRcved**</span><span class="sxs-lookup"><span data-stu-id="79e28-159">**dwPortBytesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-160">Specifica il numero totale di byte ricevuti dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-160">Specifies the total number of bytes received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-161">**dwPortFramesXmited**</span><span class="sxs-lookup"><span data-stu-id="79e28-161">**dwPortFramesXmited**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-162">Specifica il numero totale di frame trasmessi dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-162">Specifies the total number of frames transmitted by the port.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-163">**dwPortFramesRcved**</span><span class="sxs-lookup"><span data-stu-id="79e28-163">**dwPortFramesRcved**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-164">Specifica il numero totale di frame ricevuti dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-164">Specifies the total number of frames received by the port.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-165">**dwPortCrcErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-165">**dwPortCrcErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-166">Specifica il numero totale di errori CRC sulla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-166">Specifies the total number of CRC errors on the port.</span></span> <span data-ttu-id="79e28-167">Gli errori CRC sono causati dall'esito negativo di un controllo di ridondanza ciclico.</span><span class="sxs-lookup"><span data-stu-id="79e28-167">CRC errors are caused by the failure of a cyclic redundancy check.</span></span> <span data-ttu-id="79e28-168">Un errore CRC indica che uno o più caratteri nel pacchetto di dati ricevuti sono stati rilevati all'arrivo.</span><span class="sxs-lookup"><span data-stu-id="79e28-168">A CRC error indicates that one or more characters in the data packet received were found garbled on arrival.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-169">**dwPortTimeoutErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-169">**dwPortTimeoutErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-170">Specifica il numero totale di errori di timeout sulla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-170">Specifies the total number of time-out errors on the port.</span></span> <span data-ttu-id="79e28-171">Gli errori di timeout si verificano quando un carattere previsto non viene ricevuto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="79e28-171">Time-out errors occur when an expected character is not received in time.</span></span> <span data-ttu-id="79e28-172">Quando si verifica questo problema, il software presuppone che i dati siano andati perduti e che ne richieda il reinviato.</span><span class="sxs-lookup"><span data-stu-id="79e28-172">When this occurs, the software assumes that the data has been lost and requests that it be resent.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-173">**dwPortAlignmentErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-173">**dwPortAlignmentErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-174">Specifica il numero totale di errori di allineamento sulla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-174">Specifies the total number of alignment errors on the port.</span></span> <span data-ttu-id="79e28-175">Gli errori di allineamento si verificano quando un carattere ricevuto non è quello previsto.</span><span class="sxs-lookup"><span data-stu-id="79e28-175">Alignment errors occur when a character received is not the one expected.</span></span> <span data-ttu-id="79e28-176">Questa situazione si verifica in genere quando un carattere viene perso o si verifica un errore di timeout.</span><span class="sxs-lookup"><span data-stu-id="79e28-176">This usually happens when a character is lost or when a time-out error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-177">**dwPortHardwareOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-177">**dwPortHardwareOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-178">Specifica il numero totale di errori di sovraccarico hardware sulla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-178">Specifies the total number of hardware overrun errors on the port.</span></span> <span data-ttu-id="79e28-179">Questi errori indicano il numero di volte in cui il computer di invio ha trasmesso i caratteri più velocemente di quanto l'hardware del computer ricevente possa elaborarli.</span><span class="sxs-lookup"><span data-stu-id="79e28-179">These errors indicate the number of times the sending computer has transmitted characters faster than the receiving computer hardware can process them.</span></span> <span data-ttu-id="79e28-180">Se il problema persiste, ridurre la velocità di connessione BPS nel client.</span><span class="sxs-lookup"><span data-stu-id="79e28-180">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-181">**dwPortFramingErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-181">**dwPortFramingErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-182">Specifica il numero totale di errori di framing sulla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-182">Specifies the total number of framing errors on the port.</span></span> <span data-ttu-id="79e28-183">Un errore di framing si verifica quando viene ricevuto un carattere asincrono con un bit di avvio o di arresto non valido.</span><span class="sxs-lookup"><span data-stu-id="79e28-183">A framing error occurs when an asynchronous character is received with an invalid start or stop bit.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-184">**dwPortBufferOverrunErr**</span><span class="sxs-lookup"><span data-stu-id="79e28-184">**dwPortBufferOverrunErr**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-185">Specifica il numero totale di errori di sovraccarico del buffer sulla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-185">Specifies the total number of buffer overrun errors on the port.</span></span> <span data-ttu-id="79e28-186">Si verifica un errore di sovraccarico del buffer quando il computer mittente trasmette caratteri più velocemente di quanto il computer ricevente possa adattarlo.</span><span class="sxs-lookup"><span data-stu-id="79e28-186">A buffer overrun error occurs when the sending computer is transmitting characters faster than the receiving computer can accommodate them.</span></span> <span data-ttu-id="79e28-187">Se il problema persiste, ridurre la velocità di connessione BPS nel client.</span><span class="sxs-lookup"><span data-stu-id="79e28-187">If this problem persists, reduce the BPS connection rate on the client.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-188">**dwPortBytesXmitedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-188">**dwPortBytesXmitedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-189">Specifica il numero totale di byte trasmessi non compressi dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-189">Specifies the total number of bytes transmitted uncompressed by the port.</span></span> <span data-ttu-id="79e28-190">Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido.</span><span class="sxs-lookup"><span data-stu-id="79e28-190">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="79e28-191">Usare invece le statistiche di compressione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-191">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-192">**dwPortBytesRcvedUncompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-192">**dwPortBytesRcvedUncompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-193">Specifica il numero totale di byte ricevuti decompressi dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-193">Specifies the total number of bytes received uncompressed by the port.</span></span> <span data-ttu-id="79e28-194">Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido.</span><span class="sxs-lookup"><span data-stu-id="79e28-194">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="79e28-195">Usare invece le statistiche di compressione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-195">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-196">**dwPortBytesXmitedCompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-196">**dwPortBytesXmitedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-197">Specifica il numero totale di byte trasmessi dalla porta.</span><span class="sxs-lookup"><span data-stu-id="79e28-197">Specifies the total number of bytes transmitted compressed by the port.</span></span> <span data-ttu-id="79e28-198">Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido.</span><span class="sxs-lookup"><span data-stu-id="79e28-198">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="79e28-199">Usare invece le statistiche di compressione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-199">Use the compression statistics for the connection instead.</span></span>

</dd> <dt>

<span data-ttu-id="79e28-200">**dwPortBytesRcvedCompressed**</span><span class="sxs-lookup"><span data-stu-id="79e28-200">**dwPortBytesRcvedCompressed**</span></span>
</dt> <dd>

<span data-ttu-id="79e28-201">Specifica il numero totale di byte ricevuti dalla porta compressi.</span><span class="sxs-lookup"><span data-stu-id="79e28-201">Specifies the total number of bytes received compressed by the port.</span></span> <span data-ttu-id="79e28-202">Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido.</span><span class="sxs-lookup"><span data-stu-id="79e28-202">If the port is part of a multilink connection, this member is not valid.</span></span> <span data-ttu-id="79e28-203">Usare invece le statistiche di compressione per la connessione.</span><span class="sxs-lookup"><span data-stu-id="79e28-203">Use the compression statistics for the connection instead.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79e28-204">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79e28-204">Requirements</span></span>



| <span data-ttu-id="79e28-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e28-205">Requirement</span></span> | <span data-ttu-id="79e28-206">Valore</span><span class="sxs-lookup"><span data-stu-id="79e28-206">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="79e28-207">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79e28-207">Minimum supported client</span></span><br/> | <span data-ttu-id="79e28-208">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79e28-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="79e28-209">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79e28-209">Minimum supported server</span></span><br/> | <span data-ttu-id="79e28-210">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79e28-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="79e28-211">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="79e28-211">End of client support</span></span><br/>    | <span data-ttu-id="79e28-212">Windows XP</span><span class="sxs-lookup"><span data-stu-id="79e28-212">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="79e28-213">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="79e28-213">End of server support</span></span><br/>    | <span data-ttu-id="79e28-214">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79e28-214">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="79e28-215">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79e28-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="79e28-216"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e28-216"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e28-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79e28-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e28-218">Panoramica del servizio di accesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="79e28-218">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="79e28-219">Strutture di amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="79e28-219">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="79e28-220">**\_Porta RAS \_ 0**</span><span class="sxs-lookup"><span data-stu-id="79e28-220">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="79e28-221">**RasAdminAcceptNewConnection**</span><span class="sxs-lookup"><span data-stu-id="79e28-221">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="79e28-222">**RasAdminConnectionHangupNotification**</span><span class="sxs-lookup"><span data-stu-id="79e28-222">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="79e28-223">**RasAdminPortClearStatistics**</span><span class="sxs-lookup"><span data-stu-id="79e28-223">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)
</dt> <dt>

[<span data-ttu-id="79e28-224">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="79e28-224">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





