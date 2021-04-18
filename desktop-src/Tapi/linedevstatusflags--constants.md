---
description: Le \_ costanti del flag di bit LINEDEVSTATUSFLAGS descrivono una raccolta di elementi di stato dei dispositivi lineari booleani.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Costanti LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325017"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="79aee-103">\_Costanti LINEDEVSTATUSFLAGS</span><span class="sxs-lookup"><span data-stu-id="79aee-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="79aee-104">Le costanti del flag di bit **LINEDEVSTATUSFLAGS \_** descrivono una raccolta di elementi di stato dei dispositivi lineari booleani.</span><span class="sxs-lookup"><span data-stu-id="79aee-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="79aee-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="79aee-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79aee-106">Specifica se la linea è connessa a TAPI.</span><span class="sxs-lookup"><span data-stu-id="79aee-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="79aee-107">Se **true**, la linea è connessa e TAPI è in grado di operare sul dispositivo a linee.</span><span class="sxs-lookup"><span data-stu-id="79aee-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="79aee-108">Se **false**, la riga è disconnessa e l'applicazione non è in grado di controllare il dispositivo della linea tramite TAPI.</span><span class="sxs-lookup"><span data-stu-id="79aee-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79aee-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INservice**</span><span class="sxs-lookup"><span data-stu-id="79aee-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79aee-110">Indica se la riga è nel servizio.</span><span class="sxs-lookup"><span data-stu-id="79aee-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="79aee-111">Se **true**, la riga è in servizio; Se **false**, la riga è fuori servizio.</span><span class="sxs-lookup"><span data-stu-id="79aee-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79aee-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="79aee-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79aee-113">Indica se la riga è bloccata o sbloccata.</span><span class="sxs-lookup"><span data-stu-id="79aee-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="79aee-114">Questo bit viene spesso usato con i dispositivi lineari associati ai telefoni cellulari.</span><span class="sxs-lookup"><span data-stu-id="79aee-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="79aee-115">Molti telefoni cellulari hanno un meccanismo di sicurezza che richiede l'immissione di una password per consentire al telefono di inserire le chiamate.</span><span class="sxs-lookup"><span data-stu-id="79aee-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="79aee-116">Questo bit può essere utilizzato per indicare alle applicazioni che il telefono è bloccato e non è in grado di effettuare chiamate finché la password non viene immessa nell'interfaccia utente del telefono, in modo che l'applicazione possa presentare un avviso appropriato all'utente.</span><span class="sxs-lookup"><span data-stu-id="79aee-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="79aee-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**\_MSGWAIT LINEDEVSTATUSFLAGS**</span><span class="sxs-lookup"><span data-stu-id="79aee-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="79aee-118">Indica se la riga presenta un messaggio in attesa.</span><span class="sxs-lookup"><span data-stu-id="79aee-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="79aee-119">Se **true**, un messaggio è in attesa; Se **false**, nessun messaggio è in attesa.</span><span class="sxs-lookup"><span data-stu-id="79aee-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79aee-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="79aee-120">Remarks</span></span>

<span data-ttu-id="79aee-121">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="79aee-121">No extensibility.</span></span> <span data-ttu-id="79aee-122">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="79aee-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="79aee-123">Le \_ costanti LINEDEVSTATUSFLAGS vengono utilizzate all'interno del membro **dwDevStatusFlags** della struttura di dati [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="79aee-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="79aee-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79aee-124">Requirements</span></span>



| <span data-ttu-id="79aee-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="79aee-125">Requirement</span></span> | <span data-ttu-id="79aee-126">Valore</span><span class="sxs-lookup"><span data-stu-id="79aee-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="79aee-127">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="79aee-127">TAPI version</span></span><br/> | <span data-ttu-id="79aee-128">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="79aee-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="79aee-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79aee-129">Header</span></span><br/>       | <dl> <span data-ttu-id="79aee-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="79aee-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




