---
description: La \_ costante del flag di bit LINETRANSLATEOPTION descrive un'opzione utilizzata dalla conversione degli indirizzi.
ms.assetid: 3f5e9952-945e-42b8-8536-b52a0c833282
title: Costanti LINETRANSLATEOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e103f2a93d30be5260b27c7bf5c0e97f3ce7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327496"
---
# <a name="linetranslateoption_-constants"></a><span data-ttu-id="c8284-103">\_Costanti LINETRANSLATEOPTION</span><span class="sxs-lookup"><span data-stu-id="c8284-103">LINETRANSLATEOPTION\_ Constants</span></span>

<span data-ttu-id="c8284-104">La costante del flag di bit **LINETRANSLATEOPTION \_** descrive un'opzione utilizzata dalla conversione degli indirizzi.</span><span class="sxs-lookup"><span data-stu-id="c8284-104">The **LINETRANSLATEOPTION\_** bit-flag constant describes an option used by address translation.</span></span>

<dl> <dt>

<span data-ttu-id="c8284-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**\_CANCELCALLWAITING LINETRANSLATEOPTION**</span><span class="sxs-lookup"><span data-stu-id="c8284-105"><span id="LINETRANSLATEOPTION_CANCELCALLWAITING"></span><span id="linetranslateoption_cancelcallwaiting"></span>**LINETRANSLATEOPTION\_CANCELCALLWAITING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8284-106">Se per la posizione è definita una stringa di attesa di chiamata Cancel, l'impostazione di questo bit provocherà l'inserimento di tale stringa all'inizio della stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="c8284-106">If a Cancel Call Waiting string is defined for the location, setting this bit will cause that string to be inserted at the beginning of the dialable string.</span></span> <span data-ttu-id="c8284-107">Questa operazione viene in genere utilizzata dal modem dati e dalle applicazioni fax per evitare interruzioni di chiamate dai segnali acustici in attesa.</span><span class="sxs-lookup"><span data-stu-id="c8284-107">This is commonly used by data modem and fax applications to prevent interruption of calls by call waiting beeps.</span></span> <span data-ttu-id="c8284-108">Se per la posizione non è definita alcuna stringa di attesa di chiamata Cancel, questo bit non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="c8284-108">If no Cancel Call Waiting string is defined for the location, this bit has no affect.</span></span> <span data-ttu-id="c8284-109">Si noti che per le applicazioni che usano questo bit è consigliabile impostare anche il \_ bit sicuro LINECALLPARAMFLAGS nel membro **dwCallParamFlags** della struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passata a [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) tramite il parametro *lpCallParams* , in modo che, se il dispositivo della linea usa un meccanismo diverso dalle cifre che è possibile comporre per impedire l'interruzione della chiamata, il meccanismo verrà richiamato.</span><span class="sxs-lookup"><span data-stu-id="c8284-109">Note that applications using this bit are advised to also set the LINECALLPARAMFLAGS\_SECURE bit in the **dwCallParamFlags** member of the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure passed in to [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) through the *lpCallParams* parameter, so that if the line device uses a mechanism other than dialable digits to suppress call interrupts then that mechanism will be invoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8284-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**\_CARDOVERRIDE LINETRANSLATEOPTION**</span><span class="sxs-lookup"><span data-stu-id="c8284-110"><span id="LINETRANSLATEOPTION_CARDOVERRIDE"></span><span id="linetranslateoption_cardoverride"></span>**LINETRANSLATEOPTION\_CARDOVERRIDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8284-111">È necessario eseguire l'override della scheda chiamante predefinita con una specifica.</span><span class="sxs-lookup"><span data-stu-id="c8284-111">The default calling card is to be overridden with a specified one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8284-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**\_FORCELD LINETRANSLATEOPTION**</span><span class="sxs-lookup"><span data-stu-id="c8284-112"><span id="LINETRANSLATEOPTION_FORCELD"></span><span id="linetranslateoption_forceld"></span>**LINETRANSLATEOPTION\_FORCELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8284-113">Questa opzione impone che l'indirizzo (numero) venga convertito come Long distance.</span><span class="sxs-lookup"><span data-stu-id="c8284-113">This option forces the address (number) to be translated as long distance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c8284-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**\_FORCELOCAL LINETRANSLATEOPTION**</span><span class="sxs-lookup"><span data-stu-id="c8284-114"><span id="LINETRANSLATEOPTION_FORCELOCAL"></span><span id="linetranslateoption_forcelocal"></span>**LINETRANSLATEOPTION\_FORCELOCAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="c8284-115">Questa opzione impone al numero (indirizzo) di essere convertito come locale.</span><span class="sxs-lookup"><span data-stu-id="c8284-115">This option forces the number (address) to be translated as local.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8284-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8284-116">Remarks</span></span>

<span data-ttu-id="c8284-117">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="c8284-117">No extensibility.</span></span> <span data-ttu-id="c8284-118">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="c8284-118">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8284-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8284-119">Requirements</span></span>



| <span data-ttu-id="c8284-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8284-120">Requirement</span></span> | <span data-ttu-id="c8284-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c8284-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c8284-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c8284-122">TAPI version</span></span><br/> | <span data-ttu-id="c8284-123">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c8284-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="c8284-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8284-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c8284-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8284-125"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8284-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8284-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8284-127">**LINECALLPARAMS**</span><span class="sxs-lookup"><span data-stu-id="c8284-127">**LINECALLPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallparams)
</dt> <dt>

[<span data-ttu-id="c8284-128">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="c8284-128">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="c8284-129">**LINETRANSLATEOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="c8284-129">**LINETRANSLATEOUTPUT**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linetranslateoutput)
</dt> </dl>

 

 




