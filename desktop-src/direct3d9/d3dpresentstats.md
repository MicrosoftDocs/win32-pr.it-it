---
description: Descrive le statistiche di presentazione catena relative alle chiamate PresentEx.
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: Struttura D3DPRESENTSTATS (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235070"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="43fc1-103">Struttura D3DPRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="43fc1-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="43fc1-104">Descrive le statistiche di presentazione catena relative alle chiamate [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="43fc1-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="43fc1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43fc1-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="43fc1-106">Members</span><span class="sxs-lookup"><span data-stu-id="43fc1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="43fc1-107">**PresentCount**</span><span class="sxs-lookup"><span data-stu-id="43fc1-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="43fc1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43fc1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43fc1-109">Esecuzione del conteggio delle chiamate di presentazione riuscite effettuate da un dispositivo di visualizzazione attualmente in fase di output sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="43fc1-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="43fc1-110">Questo parametro è effettivamente l'ID attuale dell'ultima chiamata presente e non è necessariamente il numero totale di chiamate API effettuate.</span><span class="sxs-lookup"><span data-stu-id="43fc1-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="43fc1-111">**PresentRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="43fc1-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="43fc1-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43fc1-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43fc1-113">Il numero di vblank in corrispondenza del quale l'ultimo presente è stato visualizzato sullo schermo, il numero di vblank viene incrementato una volta ogni intervallo di vblank.</span><span class="sxs-lookup"><span data-stu-id="43fc1-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="43fc1-114">**SyncRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="43fc1-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="43fc1-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43fc1-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43fc1-116">Il numero di vblank quando l'utilità di pianificazione ha ultimo campionato l'ora del computer chiamando QueryPerformanceCounter.</span><span class="sxs-lookup"><span data-stu-id="43fc1-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="43fc1-117">**SyncQPCTime**</span><span class="sxs-lookup"><span data-stu-id="43fc1-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="43fc1-118">Tipo: **[ **\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="43fc1-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="43fc1-119">Ultimo tempo del computer Campionato dell'utilità di pianificazione, ottenuto chiamando [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="43fc1-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="43fc1-120">**SyncGPUTime**</span><span class="sxs-lookup"><span data-stu-id="43fc1-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="43fc1-121">Tipo: **[ **\_ Integer grande**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="43fc1-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="43fc1-122">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="43fc1-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43fc1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="43fc1-123">Remarks</span></span>

<span data-ttu-id="43fc1-124">Quando un'applicazione 9Ex adotta la modalità Flip presente (D3DSWAPEFFECT \_ FLIPEX), le applicazioni possono rilevare la rimozione dei frame chiamando GetPresentStatistics in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="43fc1-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="43fc1-125">In effetti, è possibile eseguire le operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="43fc1-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="43fc1-126">Eseguire il rendering nel buffer nascosto</span><span class="sxs-lookup"><span data-stu-id="43fc1-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="43fc1-127">Chiamata presente</span><span class="sxs-lookup"><span data-stu-id="43fc1-127">Call Present</span></span>
3.  <span data-ttu-id="43fc1-128">Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante</span><span class="sxs-lookup"><span data-stu-id="43fc1-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="43fc1-129">Esegue il rendering del frame successivo nel buffer nascosto</span><span class="sxs-lookup"><span data-stu-id="43fc1-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="43fc1-130">Chiamata presente</span><span class="sxs-lookup"><span data-stu-id="43fc1-130">Call Present</span></span>
6.  <span data-ttu-id="43fc1-131">Ripetere i passaggi 4 e 5 1 o più volte</span><span class="sxs-lookup"><span data-stu-id="43fc1-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="43fc1-132">Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante</span><span class="sxs-lookup"><span data-stu-id="43fc1-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="43fc1-133">Confrontare i valori di PresentRefreshCount dalle due strutture D3DPRESENTSTATS archiviate.</span><span class="sxs-lookup"><span data-stu-id="43fc1-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="43fc1-134">L'applicazione può calcolare il PresentRefreshCount corrispondente di un determinato parametro PresentCount in base ai presupposti di incremento PresentRefreshCount e assegnazione PresentCount dei presentatori frame.</span><span class="sxs-lookup"><span data-stu-id="43fc1-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="43fc1-135">Se l'ultimo esempio di PresentRefreshCount non corrisponde a PresentCount (ad esempio, se il PresentRefreshCount è stato incrementato ma PresentCount non lo è, è stato eliminato il frame).</span><span class="sxs-lookup"><span data-stu-id="43fc1-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="43fc1-136">Le applicazioni possono determinare se un frame è stato eliminato eseguendo il campionamento di due istanze di PresentCount e GetPresentStats (chiamando l'API GetPresentStats in due punti nel tempo).</span><span class="sxs-lookup"><span data-stu-id="43fc1-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="43fc1-137">Ad esempio, un'applicazione multimediale che presenta alla stessa frequenza della frequenza di aggiornamento del monitor (ad esempio, la frequenza di aggiornamento del monitoraggio è 60Hz, l'applicazione presenta un frame ogni 1/60 secondi) desidera presentare i frame a, B, C, D, E, ognuno dei quali corrisponde agli ID presenti (PresentCount) 1, 2, 3, 7, 8.</span><span class="sxs-lookup"><span data-stu-id="43fc1-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="43fc1-138">Il codice dell'applicazione ha un aspetto analogo alla sequenza seguente.</span><span class="sxs-lookup"><span data-stu-id="43fc1-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="43fc1-139">Eseguire il rendering del frame a nel buffer nascosto</span><span class="sxs-lookup"><span data-stu-id="43fc1-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="43fc1-140">Chiamata presente, PresentCount = 1</span><span class="sxs-lookup"><span data-stu-id="43fc1-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="43fc1-141">Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante</span><span class="sxs-lookup"><span data-stu-id="43fc1-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="43fc1-142">Eseguire il rendering dei 4 frame successivi, B, C, D, E, rispettivamente</span><span class="sxs-lookup"><span data-stu-id="43fc1-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="43fc1-143">Call present 4 volte, PresentCounts = 2, 3, 7, 8, rispettivamente</span><span class="sxs-lookup"><span data-stu-id="43fc1-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="43fc1-144">Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante</span><span class="sxs-lookup"><span data-stu-id="43fc1-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="43fc1-145">Confrontare i valori di PresentRefreshCount dalle due strutture D3DPRESENTSTATS archiviate.</span><span class="sxs-lookup"><span data-stu-id="43fc1-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="43fc1-146">Se la differenza è 2, ovvero sono trascorsi 2 intervalli vblank tra le due chiamate API GetPresentStats, l'ultimo frame presentato dovrebbe essere il frame C. Poiché l'applicazione presenta un intervallo di vblank (la frequenza di aggiornamento del monitoraggio), il tempo trascorso tra il frame A viene presentato e quando viene presentato il frame C dovrebbe essere 2 vblanks.</span><span class="sxs-lookup"><span data-stu-id="43fc1-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="43fc1-147">Confrontare i valori di PresentCount dalle due strutture D3DPRESENTSTATS archiviate.</span><span class="sxs-lookup"><span data-stu-id="43fc1-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="43fc1-148">Se il primo PresentCount è 1 (corrispondente al frame A) e il secondo PresentCount è 3 (corrispondente al frame C), non sono stati eliminati frame.</span><span class="sxs-lookup"><span data-stu-id="43fc1-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="43fc1-149">Se il secondo PresentCount è 3, che corrisponde al frame D, l'applicazione sa che un frame è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="43fc1-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="43fc1-150">Si noti che GetPresentStatistics verrà elaborato dopo che è stato chiamato, indipendentemente dallo stato delle chiamate PresentEx in modalità FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="43fc1-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="43fc1-151">**Windows Vista:** Le chiamate attuali verranno accodate e quindi elaborate prima che venga elaborata la chiamata GetPresentStats.</span><span class="sxs-lookup"><span data-stu-id="43fc1-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="43fc1-152">Quando un'applicazione rileva che la presentazione di determinati frame è dietro, può ignorare tali frame e correggere la presentazione per eseguire nuovamente la sincronizzazione con vblank.</span><span class="sxs-lookup"><span data-stu-id="43fc1-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="43fc1-153">A tale scopo, un'applicazione non può semplicemente eseguire il rendering dei frame tardivi e avviare il rendering con il frame corretto successivo nella coda.</span><span class="sxs-lookup"><span data-stu-id="43fc1-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="43fc1-154">Tuttavia, se un'applicazione ha già avviato il rendering dei frame tardivi, può usare un nuovo parametro presente in D3D9Ex denominato D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="43fc1-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="43fc1-155">Il flag verrà passato nei parametri della chiamata API presente e indicherà al runtime che il frame verrà elaborato immediatamente entro l'intervallo di vblank successivo, in realtà non visibile sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="43fc1-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="43fc1-156">Di seguito è riportato l'esempio di utilizzo dell'applicazione dopo l'ultimo passaggio dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="43fc1-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="43fc1-157">Esegue il rendering del frame successivo nel buffer nascosto</span><span class="sxs-lookup"><span data-stu-id="43fc1-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="43fc1-158">Individuare da PresentRefreshCount che il frame successivo è già in ritardo</span><span class="sxs-lookup"><span data-stu-id="43fc1-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="43fc1-159">Imposta l'intervallo presente su D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="43fc1-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="43fc1-160">Chiamata presente nel frame successivo</span><span class="sxs-lookup"><span data-stu-id="43fc1-160">Call Present on the next frame</span></span>

<span data-ttu-id="43fc1-161">Le applicazioni possono sincronizzare flussi video e audio nello stesso modo, perché il comportamento di GetPresentStatistics non cambia in questo scenario.</span><span class="sxs-lookup"><span data-stu-id="43fc1-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="43fc1-162">La modalità D3D9Ex Flip fornisce informazioni sulle statistiche sui frame per le applicazioni con finestra e le applicazioni 9Ex a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="43fc1-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="43fc1-163">**Windows Vista:** Utilizzare le API di DWM per recuperare le statistiche presenti.</span><span class="sxs-lookup"><span data-stu-id="43fc1-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="43fc1-164">Quando Gestione finestre desktop è disattivato, le applicazioni 9Ex in modalità finestra che usano la modalità Flip riceveranno le informazioni sulle statistiche di accuratezza limitata.</span><span class="sxs-lookup"><span data-stu-id="43fc1-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="43fc1-165">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="43fc1-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="43fc1-166">Se un'applicazione non è sufficientemente veloce da soddisfare la frequenza di aggiornamento del monitoraggio, probabilmente a causa di hardware lento o di risorse di sistema insufficienti, è possibile che si verifichi un problema di grafica.</span><span class="sxs-lookup"><span data-stu-id="43fc1-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="43fc1-167">Un problema è un singhiozzo visivo così chiamato.</span><span class="sxs-lookup"><span data-stu-id="43fc1-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="43fc1-168">Se un monitoraggio è impostato per l'aggiornamento a 60 Hz e l'applicazione può gestire solo 30 fps, la metà dei frame avrà problemi.</span><span class="sxs-lookup"><span data-stu-id="43fc1-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="43fc1-169">Le applicazioni possono rilevare un problema tenendo traccia dei SynchRefreshCount.</span><span class="sxs-lookup"><span data-stu-id="43fc1-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="43fc1-170">Ad esempio, un'applicazione potrebbe eseguire la sequenza di azioni seguente.</span><span class="sxs-lookup"><span data-stu-id="43fc1-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="43fc1-171">Eseguire il rendering nel buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="43fc1-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="43fc1-172">Chiamata presente.</span><span class="sxs-lookup"><span data-stu-id="43fc1-172">Call Present.</span></span>
3.  <span data-ttu-id="43fc1-173">Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante.</span><span class="sxs-lookup"><span data-stu-id="43fc1-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="43fc1-174">Esegue il rendering del frame successivo nel buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="43fc1-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="43fc1-175">Chiamata presente.</span><span class="sxs-lookup"><span data-stu-id="43fc1-175">Call Present.</span></span>
6.  <span data-ttu-id="43fc1-176">Chiamare GetPresentStats e archiviare la struttura D3DPRESENTSTATS risultante.</span><span class="sxs-lookup"><span data-stu-id="43fc1-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="43fc1-177">Confrontare i valori di SyncRefreshCount dalle due strutture D3DPRESENTSTATS archiviate.</span><span class="sxs-lookup"><span data-stu-id="43fc1-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="43fc1-178">Se la differenza è maggiore di uno, un frame è stato ignorato.</span><span class="sxs-lookup"><span data-stu-id="43fc1-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="43fc1-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43fc1-179">Requirements</span></span>



| <span data-ttu-id="43fc1-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fc1-180">Requirement</span></span> | <span data-ttu-id="43fc1-181">Valore</span><span class="sxs-lookup"><span data-stu-id="43fc1-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43fc1-182">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43fc1-182">Header</span></span><br/> | <dl> <span data-ttu-id="43fc1-183"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="43fc1-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43fc1-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43fc1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43fc1-185">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="43fc1-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
