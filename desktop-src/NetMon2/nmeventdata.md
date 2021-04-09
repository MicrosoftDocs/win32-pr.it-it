---
description: La struttura NMEVENTDATA contiene informazioni su una condizione dell'evento che viene passata a Network Monitor per inserire una riga nel Visualizzatore esperti.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Struttura NMEVENTDATA (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879674"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="3d7d0-103">Struttura NMEVENTDATA</span><span class="sxs-lookup"><span data-stu-id="3d7d0-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="3d7d0-104">La struttura **NMEVENTDATA** contiene informazioni su una condizione dell'evento che viene passata a Network Monitor per inserire una riga nel Visualizzatore esperti.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d7d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d7d0-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="3d7d0-106">Members</span><span class="sxs-lookup"><span data-stu-id="3d7d0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d7d0-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-108">Numero di versione della struttura **NMEVENTDATA** .</span><span class="sxs-lookup"><span data-stu-id="3d7d0-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="3d7d0-109">Il numero di versione deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-109">The version number must be zero.</span></span> <span data-ttu-id="3d7d0-110">Le versioni future di Network Monitor possono supportare un numero di versione superiore.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-111">**EventIdent**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-112">Identificatore dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-112">Identifier of the event.</span></span> <span data-ttu-id="3d7d0-113">**EventIdent** è univoco per ogni esperto e fa riferimento a una [pagina di riferimento](event-reference-page.md)a un evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-115">Set di flag che descrive chi invia i dati dell'evento e come viene visualizzato l'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="3d7d0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3d7d0-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="3d7d0-117">Significato</span><span class="sxs-lookup"><span data-stu-id="3d7d0-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="3d7d0-118"><dt>**\_esperto flag di evento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="3d7d0-119">L'evento proviene da un esperto.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="3d7d0-120"><dt>**NMEVENTFLAG \_ \_ non \_ visualizzano la \_ gravità**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="3d7d0-121">Non visualizzare il livello di gravità per l'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="3d7d0-122"><dt>**NMEVENTFLAG \_ \_ non \_ Visualizza l' \_ origine**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="3d7d0-123">Non visualizzare il nome dell'origine per l'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="3d7d0-124"><dt>**NMEVENTFLAG \_ \_ non \_ Visualizza il \_ nome dell'evento \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="3d7d0-125">Non visualizzare il nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="3d7d0-126"><dt>**NMEVENTFLAG \_ \_ non \_ Visualizza la \_ Descrizione**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="3d7d0-127">Non visualizzare la descrizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="3d7d0-128"><dt>**NMEVENTFLAG \_ \_ non \_ Visualizza il \_ computer**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="3d7d0-129">Non visualizzare il nome del computer per l'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="3d7d0-130"><dt>**NMEVENTFLAG \_ \_ non \_ Visualizza l' \_ ora**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="3d7d0-131">Non visualizzare l'ora dell'evento</span><span class="sxs-lookup"><span data-stu-id="3d7d0-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="3d7d0-132"><dt>**NMEVENTFLAG \_ \_ non \_ Visualizza \_ colonne fisse \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="3d7d0-133">Non visualizzare la gravità, l'origine, il nome dell'evento, la descrizione, il computer o le colonne temporali.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="3d7d0-134">Non si tratta di un flag singolo, ma è un'Unione dei sei flag precedenti.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="3d7d0-135">**Gravità**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-136">Livello di gravità dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-136">Severity level of the event.</span></span> <span data-ttu-id="3d7d0-137">Il livello di gravità può avere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d7d0-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="3d7d0-138">gravità \_ NMEVENT \_ Informational NMEVENT \_ \_ avviso NMEVENT gravità \_ \_ \_ grave avviso NMEVENT \_ gravità \_ errore NMEVENT \_ gravità grave errore NMEVENT gravità \_ \_ \_ \_ errore critico \_</span><span class="sxs-lookup"><span data-stu-id="3d7d0-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-139">**NumColumns**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-140">Numero di colonne designate nella struttura corrente.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-141">**szSourceName**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-142">Nome dell'esperto visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-143">**szEventName**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-144">Nome dell'evento visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-145">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-146">Descrizione dell'evento visualizzato.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-147">**szMachine**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-148">Obsoleto, deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-149">**Giustificazione**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-150">Informazioni visualizzate nella seconda finestra del Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="3d7d0-151">Il membro **giustificazione** può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="3d7d0-152">Se è **null**, la seconda finestra non è visibile.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-153">**szUrl**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-154">Riservati Questo membro deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-155">**SysTime**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-156">Ora in cui si verifica la condizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="3d7d0-157">Il tempo viene misurato in relazione all'inizio dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="3d7d0-158">**Colonna**</span><span class="sxs-lookup"><span data-stu-id="3d7d0-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="3d7d0-159">Tabella delle strutture di colonna visualizzata nel riquadro superiore del Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="3d7d0-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d7d0-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d7d0-160">Requirements</span></span>



| <span data-ttu-id="3d7d0-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d7d0-161">Requirement</span></span> | <span data-ttu-id="3d7d0-162">Valore</span><span class="sxs-lookup"><span data-stu-id="3d7d0-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7d0-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d7d0-163">Minimum supported client</span></span><br/> | <span data-ttu-id="3d7d0-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d7d0-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3d7d0-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d7d0-165">Minimum supported server</span></span><br/> | <span data-ttu-id="3d7d0-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3d7d0-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d7d0-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d7d0-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d7d0-168"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d7d0-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 




