---
description: Il metodo ManageChannel costruisce un comando APDU (Application Protocol Data Unit) che consente di aprire e chiudere i canali logici.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'Metodo ISCardISO7816:: ManageChannel (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049822"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="cd318-103">Metodo ISCardISO7816:: ManageChannel</span><span class="sxs-lookup"><span data-stu-id="cd318-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="cd318-104">\[Il metodo **ManageChannel** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="cd318-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd318-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cd318-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd318-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="cd318-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cd318-107">Il metodo **ManageChannel** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che consente di aprire e chiudere i canali logici.</span><span class="sxs-lookup"><span data-stu-id="cd318-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="cd318-108">La funzione Open apre un nuovo canale logico diverso da quello di base.</span><span class="sxs-lookup"><span data-stu-id="cd318-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="cd318-109">Sono disponibili opzioni per la scheda per assegnare un numero di canale logico o per il numero di canale logico da fornire alla scheda.</span><span class="sxs-lookup"><span data-stu-id="cd318-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="cd318-110">La funzione close chiude in modo esplicito un canale logico diverso da quello di base.</span><span class="sxs-lookup"><span data-stu-id="cd318-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="cd318-111">Una volta completata la chiusura, il canale logico sarà disponibile per il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="cd318-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd318-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd318-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="cd318-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd318-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd318-114">*byChannelState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd318-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd318-115">Bit B8 di P1 viene usato per indicare la funzione Open o la funzione close; Se B8 è 0, il canale di gestione deve aprire un canale logico e se B8 è 1, il canale di gestione deve chiudere un canale logico:</span><span class="sxs-lookup"><span data-stu-id="cd318-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="cd318-116">P1 = "00" da aprire</span><span class="sxs-lookup"><span data-stu-id="cd318-116">P1 = '00' to open</span></span>

<span data-ttu-id="cd318-117">P1 = "80" da chiudere</span><span class="sxs-lookup"><span data-stu-id="cd318-117">P1 = '80' to close</span></span>

<span data-ttu-id="cd318-118">Altri valori sono RFU</span><span class="sxs-lookup"><span data-stu-id="cd318-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="cd318-119">*byChannel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd318-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd318-120">Per la funzione Open (P1 = "00"), i bit B1 e B2 di P2 vengono usati per codificare il numero di canale logico nello stesso modo in cui si trova nella classe byte, mentre gli altri bit di P2 sono RFU.</span><span class="sxs-lookup"><span data-stu-id="cd318-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="cd318-121">Quando B1 e B2 di P2 sono **null**, la scheda assegnerà un numero di canale logico che verrà restituito in bits B1 e B2 del campo dati.</span><span class="sxs-lookup"><span data-stu-id="cd318-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="cd318-122">Quando B1 e/o B2 di P2 non sono **null**, codificano un numero di canale logico diverso da quello di base; la scheda apre quindi il numero di canale logico assegnato dall'esterno.</span><span class="sxs-lookup"><span data-stu-id="cd318-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="cd318-123">*ppCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="cd318-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd318-124">In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.</span><span class="sxs-lookup"><span data-stu-id="cd318-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="cd318-125">Al ritorno, viene compilato con il comando APDU creato da questa operazione.</span><span class="sxs-lookup"><span data-stu-id="cd318-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="cd318-126">Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="cd318-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd318-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd318-127">Return value</span></span>

<span data-ttu-id="cd318-128">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd318-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cd318-129">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cd318-129">Return code</span></span>                                                                                   | <span data-ttu-id="cd318-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd318-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cd318-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cd318-132">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="cd318-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cd318-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cd318-134">Parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="cd318-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="cd318-135"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cd318-136">È stato passato un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="cd318-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="cd318-137"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cd318-138">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="cd318-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="cd318-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd318-139">Remarks</span></span>

<span data-ttu-id="cd318-140">Quando la funzione Open viene eseguita correttamente dal canale logico di base, MF deve essere selezionato in modo implicito come DF corrente e lo stato di sicurezza del nuovo canale logico deve essere lo stesso del canale logico di base dopo ATR.</span><span class="sxs-lookup"><span data-stu-id="cd318-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="cd318-141">Lo stato di sicurezza del nuovo canale logico deve essere diverso da quello di qualsiasi altro canale logico.</span><span class="sxs-lookup"><span data-stu-id="cd318-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="cd318-142">Quando la funzione Open viene eseguita correttamente da un canale logico, che non è quello di base, il valore DF corrente del canale logico che ha emesso il comando verrà selezionato come DF corrente.</span><span class="sxs-lookup"><span data-stu-id="cd318-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="cd318-143">Inoltre, lo stato di sicurezza per il nuovo canale logico deve corrispondere allo stato di sicurezza del canale logico da cui è stata eseguita la funzione di apertura.</span><span class="sxs-lookup"><span data-stu-id="cd318-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="cd318-144">Dopo una funzione di chiusura corretta, lo stato di sicurezza correlato a questo canale logico viene perso.</span><span class="sxs-lookup"><span data-stu-id="cd318-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="cd318-145">Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="cd318-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="cd318-146">Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd318-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cd318-147">Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cd318-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd318-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd318-148">Requirements</span></span>



| <span data-ttu-id="cd318-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd318-149">Requirement</span></span> | <span data-ttu-id="cd318-150">Valore</span><span class="sxs-lookup"><span data-stu-id="cd318-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd318-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd318-151">Minimum supported client</span></span><br/> | <span data-ttu-id="cd318-152">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd318-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cd318-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd318-153">Minimum supported server</span></span><br/> | <span data-ttu-id="cd318-154">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cd318-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd318-155">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cd318-155">End of client support</span></span><br/>    | <span data-ttu-id="cd318-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd318-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cd318-157">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cd318-157">End of server support</span></span><br/>    | <span data-ttu-id="cd318-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cd318-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cd318-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd318-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd318-160"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd318-161">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cd318-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd318-162"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cd318-163">DLL</span><span class="sxs-lookup"><span data-stu-id="cd318-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd318-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd318-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd318-165">IID</span><span class="sxs-lookup"><span data-stu-id="cd318-165">IID</span></span><br/>                      | <span data-ttu-id="cd318-166">IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cd318-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="cd318-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd318-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd318-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="cd318-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
