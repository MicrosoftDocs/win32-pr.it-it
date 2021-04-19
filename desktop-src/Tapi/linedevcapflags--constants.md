---
description: Le \_ costanti dei flag di bit LINEDEVCAPFLAGS sono una raccolta di valori booleani che descrivono diverse funzionalità del dispositivo line.
ms.assetid: 0c537488-9fb9-4961-bd0a-1937aefc0b08
title: Costanti LINEDEVCAPFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffefca75c00fdf09b1886affbff7f0ea90bab6c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332724"
---
# <a name="linedevcapflags_-constants"></a><span data-ttu-id="52792-103">\_Costanti LINEDEVCAPFLAGS</span><span class="sxs-lookup"><span data-stu-id="52792-103">LINEDEVCAPFLAGS\_ Constants</span></span>

<span data-ttu-id="52792-104">Le costanti dei flag di bit **LINEDEVCAPFLAGS \_** sono una raccolta di valori booleani che descrivono diverse funzionalità del dispositivo line.</span><span class="sxs-lookup"><span data-stu-id="52792-104">The **LINEDEVCAPFLAGS\_** bit-flag constants are a collection of Booleans describing various line device capabilities.</span></span>

<dl> <dt>

<span data-ttu-id="52792-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**\_CALLHUB LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-105"><span id="LINEDEVCAPFLAGS_CALLHUB"></span><span id="linedevcapflags_callhub"></span>**LINEDEVCAPFLAGS\_CALLHUB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-106">Indica se gli hub di chiamata sono supportati in questa riga.</span><span class="sxs-lookup"><span data-stu-id="52792-106">Indicates whether call hubs are supported on this line.</span></span> <span data-ttu-id="52792-107">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="52792-107">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**\_CALLHUBTRACKING LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-108"><span id="LINEDEVCAPFLAGS_CALLHUBTRACKING"></span><span id="linedevcapflags_callhubtracking"></span>**LINEDEVCAPFLAGS\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-109">Indica se la verifica dell'hub chiamate è supportata in questa riga.</span><span class="sxs-lookup"><span data-stu-id="52792-109">Indicates whether call hub tracking is supported on this line.</span></span> <span data-ttu-id="52792-110">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="52792-110">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**\_CLOSEDROP LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-111"><span id="LINEDEVCAPFLAGS_CLOSEDROP"></span><span id="linedevcapflags_closedrop"></span>**LINEDEVCAPFLAGS\_CLOSEDROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-112">Specifica cosa accade quando una linea aperta viene chiusa mentre l'applicazione ha chiamate attive sulla riga.</span><span class="sxs-lookup"><span data-stu-id="52792-112">Specifies what happens when an open line is closed while the application has calls active on the line.</span></span> <span data-ttu-id="52792-113">Se **true**, il provider di servizi Elimina (Cancella) tutte le chiamate attive sulla riga quando l'ultima applicazione che ha aperto la riga la chiude con [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span><span class="sxs-lookup"><span data-stu-id="52792-113">If **TRUE**, the service provider drops (clears) all active calls on the line when the last application that has opened the line closes it with [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose).</span></span> <span data-ttu-id="52792-114">Se **false**, il provider di servizi non elimina le chiamate attive in tali casi.</span><span class="sxs-lookup"><span data-stu-id="52792-114">If **FALSE**, the service provider does not drop active calls in such cases.</span></span> <span data-ttu-id="52792-115">Al contrario, le chiamate rimangono attive e controllano i dispositivi esterni.</span><span class="sxs-lookup"><span data-stu-id="52792-115">Instead, the calls remain active and under control of external devices.</span></span> <span data-ttu-id="52792-116">Un provider di servizi imposta in genere questo bit su **false** se è presente un altro dispositivo che può mantenerla attiva. ad esempio, se una linea analoga ha il computer e il set di telefono entrambi si connettono direttamente a essi in una configurazione a livello di entità, il telefono Offhook manterrà automaticamente la chiamata attiva anche dopo il rallentamento del computer.</span><span class="sxs-lookup"><span data-stu-id="52792-116">A service provider typically sets this bit to **FALSE** if there is some other device that can keep the call alive, for example, if an analog line has the computer and phone set both connect directly to them in a party-line configuration, the offhook phone will automatically keep the call active even after the computer powers down.</span></span>

<span data-ttu-id="52792-117">Le applicazioni devono selezionare questo flag per determinare se avvisare l'utente (con una finestra di dialogo OK/Annulla) che le chiamate attive andranno perse.</span><span class="sxs-lookup"><span data-stu-id="52792-117">Applications should check this flag to determine whether to warn the user (with an OK/Cancel dialog box) that active calls will be lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**\_CROSSADDRCONF LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-118"><span id="LINEDEVCAPFLAGS_CROSSADDRCONF"></span><span id="linedevcapflags_crossaddrconf"></span>**LINEDEVCAPFLAGS\_CROSSADDRCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-119">Specifica se le chiamate su indirizzi diversi in questa riga possono essere contrattate.</span><span class="sxs-lookup"><span data-stu-id="52792-119">Specifies whether calls on different addresses on this line can be conferenced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**\_DIALBILLING LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-120"><span id="LINEDEVCAPFLAGS_DIALBILLING"></span><span id="linedevcapflags_dialbilling"></span>**LINEDEVCAPFLAGS\_DIALBILLING**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**\_DIALDIALTONE LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-121"><span id="LINEDEVCAPFLAGS_DIALDIALTONE"></span><span id="linedevcapflags_dialdialtone"></span>**LINEDEVCAPFLAGS\_DIALDIALTONE**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**\_DIALQUIET LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-122"><span id="LINEDEVCAPFLAGS_DIALQUIET"></span><span id="linedevcapflags_dialquiet"></span>**LINEDEVCAPFLAGS\_DIALQUIET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-123">Questi flag indicano se il modificatore di stringa componibile "$", "@" o "W" è supportato per una determinata periferica di linea.</span><span class="sxs-lookup"><span data-stu-id="52792-123">These flags indicate whether the "$", "@", or "W" dialable string modifier is supported for a given line device.</span></span> <span data-ttu-id="52792-124">È **true** se il modificatore è supportato; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="52792-124">It is **TRUE** if the modifier is supported; otherwise, **FALSE**.</span></span> <span data-ttu-id="52792-125">"?" (Richiedi all'utente di continuare la composizione) non è mai supportato da un dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="52792-125">The "?" (prompt user to continue dialing) is never supported by a line device.</span></span> <span data-ttu-id="52792-126">Questi flag consentono a un'applicazione di determinare prima di tutto i modificatori comportano la generazione di un LINEERR.</span><span class="sxs-lookup"><span data-stu-id="52792-126">These flags allow an application to determine up front which modifiers would result in the generation of a LINEERR.</span></span> <span data-ttu-id="52792-127">Nell'applicazione è possibile scegliere di eseguire la pre-analisi delle stringhe che è possibile comporre per i caratteri non supportati o di passare la stringa "non elaborata" da [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) direttamente al provider come parte di funzioni quali [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) o [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) e lasciare che la funzione generi un errore per indicare quale modificatore non supportato si verifica per primo nella stringa.</span><span class="sxs-lookup"><span data-stu-id="52792-127">The application has the choice of pre-scanning dialable strings for unsupported characters or of passing the "raw" string from [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) directly to the provider as part of functions such as [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) or [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial) and let the function generate an error to tell it which unsupported modifier occurs first in the string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**\_HIGHLEVCOMP LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-128"><span id="LINEDEVCAPFLAGS_HIGHLEVCOMP"></span><span id="linedevcapflags_highlevcomp"></span>**LINEDEVCAPFLAGS\_HIGHLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-129">Specifica se in questa riga sono supportati gli elementi di informazioni sulla compatibilità di alto livello.</span><span class="sxs-lookup"><span data-stu-id="52792-129">Specifies whether high-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**\_LOWLEVCOMP LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-130"><span id="LINEDEVCAPFLAGS_LOWLEVCOMP"></span><span id="linedevcapflags_lowlevcomp"></span>**LINEDEVCAPFLAGS\_LOWLEVCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-131">Specifica se gli elementi di informazioni sulla compatibilità di basso livello sono supportati in questa riga.</span><span class="sxs-lookup"><span data-stu-id="52792-131">Specifies whether low-level compatibility information elements are supported on this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**\_MEDIACONTROL LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-132"><span id="LINEDEVCAPFLAGS_MEDIACONTROL"></span><span id="linedevcapflags_mediacontrol"></span>**LINEDEVCAPFLAGS\_MEDIACONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-133">Specifica se le operazioni di controllo del supporto sono disponibili per le chiamate a questa riga.</span><span class="sxs-lookup"><span data-stu-id="52792-133">Specifies whether media-control operations are available for calls at this line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**\_msp LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-134"><span id="LINEDEVCAPFLAGS_MSP"></span><span id="linedevcapflags_msp"></span>**LINEDEVCAPFLAGS\_MSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-135">Indica se un provider di servizi multimediali (MSP) è associato alla riga.</span><span class="sxs-lookup"><span data-stu-id="52792-135">Indicates whether a Media Service Provider (MSP) is associated with the line.</span></span> <span data-ttu-id="52792-136">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="52792-136">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**\_MULTIPLEADDR LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-137"><span id="LINEDEVCAPFLAGS_MULTIPLEADDR"></span><span id="linedevcapflags_multipleaddr"></span>**LINEDEVCAPFLAGS\_MULTIPLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-138">Specifica se [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)o [**TSPI \_ lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) è in grado di gestire più indirizzi contemporaneamente (come per il multiplexing inverso).</span><span class="sxs-lookup"><span data-stu-id="52792-138">Specifies whether [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineDial**](/windows/desktop/api/Tapi/nf-tapi-linedial), [**TSPI\_lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall), or [**TSPI\_lineDial**](/windows/win32/api/tspi/nf-tspi-tspi_linedial) is able to deal with multiple addresses at once (as for inverse multiplexing).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="52792-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**\_PRIVATEOBJECTS LINEDEVCAPFLAGS**</span><span class="sxs-lookup"><span data-stu-id="52792-139"><span id="LINEDEVCAPFLAGS_PRIVATEOBJECTS"></span><span id="linedevcapflags_privateobjects"></span>**LINEDEVCAPFLAGS\_PRIVATEOBJECTS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="52792-140">Indica se le [interfacce specifiche del provider](./provider-specific-interfaces.md) sono state implementate.</span><span class="sxs-lookup"><span data-stu-id="52792-140">Indicates whether [provider-specific Interfaces](./provider-specific-interfaces.md) have been implemented.</span></span> <span data-ttu-id="52792-141">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="52792-141">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="52792-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="52792-142">Remarks</span></span>

<span data-ttu-id="52792-143">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="52792-143">No extensibility.</span></span> <span data-ttu-id="52792-144">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="52792-144">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="52792-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52792-145">Requirements</span></span>



| <span data-ttu-id="52792-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="52792-146">Requirement</span></span> | <span data-ttu-id="52792-147">Valore</span><span class="sxs-lookup"><span data-stu-id="52792-147">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="52792-148">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="52792-148">TAPI version</span></span><br/> | <span data-ttu-id="52792-149">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="52792-149">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="52792-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52792-150">Header</span></span><br/>       | <dl> <span data-ttu-id="52792-151"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="52792-151"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52792-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52792-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52792-153">**lineClose**</span><span class="sxs-lookup"><span data-stu-id="52792-153">**lineClose**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[<span data-ttu-id="52792-154">**lineDial**</span><span class="sxs-lookup"><span data-stu-id="52792-154">**lineDial**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedial)
</dt> <dt>

[<span data-ttu-id="52792-155">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="52792-155">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="52792-156">**lineTranslateAddress**</span><span class="sxs-lookup"><span data-stu-id="52792-156">**lineTranslateAddress**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)
</dt> </dl>

 

