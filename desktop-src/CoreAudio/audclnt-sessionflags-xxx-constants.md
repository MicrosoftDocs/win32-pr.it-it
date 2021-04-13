---
description: Le \_ costanti AUDCLNT SESSIONFLAGS \_ xxx indicano le caratteristiche di una sessione audio associata al flusso.
ms.assetid: 5745d5bc-71e8-4b33-8227-c1c84226b6ee
title: Costanti AUDCLNT_SESSIONFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2152c33103ca3366399995b7d11bb072f2bdd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483924"
---
# <a name="audclnt_sessionflags_xxx-constants"></a><span data-ttu-id="9320c-103">\_Costanti AUDCLNT SESSIONFLAGS \_ xxx</span><span class="sxs-lookup"><span data-stu-id="9320c-103">AUDCLNT\_SESSIONFLAGS\_XXX Constants</span></span>

<span data-ttu-id="9320c-104">Le \_ costanti AUDCLNT SESSIONFLAGS \_ xxx indicano le caratteristiche di una sessione audio associata al flusso.</span><span class="sxs-lookup"><span data-stu-id="9320c-104">The AUDCLNT\_SESSIONFLAGS\_XXX constants indicate characteristics of an audio session associated with the stream.</span></span> <span data-ttu-id="9320c-105">Un client può specificare queste opzioni durante l'inizializzazione del flusso tramite il parametro *StreamFlags* del metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) .</span><span class="sxs-lookup"><span data-stu-id="9320c-105">A client can specify these options during the initialization of the stream by through the *StreamFlags* parameter of the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method.</span></span>



| <span data-ttu-id="9320c-106">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="9320c-106">Constant/value</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="9320c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9320c-107">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_SESSIONFLAGS_EXPIREWHENUNOWNED"></span><span id="audclnt_sessionflags_expirewhenunowned"></span><dl> <span data-ttu-id="9320c-108"><dt>**AUDCLNT \_ SESSIONFLAGS \_ EXPIREWHENUNOWNED**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="9320c-108"><dt>**AUDCLNT\_SESSIONFLAGS\_EXPIREWHENUNOWNED**</dt> <dt>0x10000000 </dt></span></span> </dl>                       | <span data-ttu-id="9320c-109">La sessione scade quando non sono presenti flussi associati e oggetti di controllo della sessione proprietari che contengano riferimenti.</span><span class="sxs-lookup"><span data-stu-id="9320c-109">The session expires when there are no associated streams and owning session control objects holding references.</span></span><br/>                                                                                                                                                                                       |
| <span id="AUDCLNT_SESSIONFLAGS_DISPLAY_HIDE"></span><span id="audclnt_sessionflags_display_hide"></span><dl> <span data-ttu-id="9320c-110"><dt>**AUDCLNT \_ \_Visualizzazione SESSIONFLAGS \_ Hide**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="9320c-110"><dt>**AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDE**</dt> <dt>0x20000000 </dt></span></span> </dl>                                     | <span data-ttu-id="9320c-111">Il controllo volume è nascosto nell'interfaccia utente del mixer del volume quando viene creata la sessione audio.</span><span class="sxs-lookup"><span data-stu-id="9320c-111">The volume control is hidden in the volume mixer user interface when the audio session is created.</span></span> <span data-ttu-id="9320c-112">Se la sessione associata al flusso esiste già prima che [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Apra il flusso, il controllo volume viene visualizzato nel mixer del volume.</span><span class="sxs-lookup"><span data-stu-id="9320c-112">If the session associated with the stream already exists before [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) opens the stream, the volume control is displayed in the volume mixer.</span></span><br/> |
| <span id="_AUDCLNT_SESSIONFLAGS_DISPLAY_HIDEWHENEXPIRED"></span><span id="_audclnt_sessionflags_display_hidewhenexpired"></span><dl> <span data-ttu-id="9320c-113"><dt> **AUDCLNT \_ SESSIONFLAGS \_ display \_ HIDEWHENEXPIRED**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="9320c-113"><dt> **AUDCLNT\_SESSIONFLAGS\_DISPLAY\_HIDEWHENEXPIRED**</dt> <dt>0x40000000 </dt></span></span> </dl> | <span data-ttu-id="9320c-114">Il controllo volume è nascosto nell'interfaccia utente del mixer del volume dopo la scadenza della sessione.</span><span class="sxs-lookup"><span data-stu-id="9320c-114">The volume control is hidden in the volume mixer user interface after the session expires.</span></span> <br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="9320c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9320c-115">Requirements</span></span>



| <span data-ttu-id="9320c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9320c-116">Requirement</span></span> | <span data-ttu-id="9320c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9320c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9320c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9320c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9320c-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9320c-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9320c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9320c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9320c-121">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9320c-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9320c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9320c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9320c-123"><dt>Audiosessiontypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9320c-123"><dt>Audiosessiontypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9320c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9320c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9320c-125">Costanti audio Core</span><span class="sxs-lookup"><span data-stu-id="9320c-125">Core Audio Constants</span></span>](core-audio-constants.md)
</dt> <dt>

[<span data-ttu-id="9320c-126">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="9320c-126">**IAudioSessionControl**</span></span>](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
</dt> </dl>

 

 




