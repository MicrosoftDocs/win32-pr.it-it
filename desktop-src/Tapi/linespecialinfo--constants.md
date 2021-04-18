---
description: Le \_ costanti dei flag di bit di LINESPECIALINFO descrivono i segnali di informazioni speciali che la rete può usare per segnalare varie operazioni di Reporting e di osservazione della rete.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Costanti LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326882"
---
# <a name="linespecialinfo_-constants"></a><span data-ttu-id="30e59-103">\_Costanti LINESPECIALINFO</span><span class="sxs-lookup"><span data-stu-id="30e59-103">LINESPECIALINFO\_ Constants</span></span>

<span data-ttu-id="30e59-104">Le costanti dei flag di bit di **LINESPECIALINFO \_** descrivono i segnali di informazioni speciali che la rete può usare per segnalare varie operazioni di Reporting e di osservazione della rete.</span><span class="sxs-lookup"><span data-stu-id="30e59-104">The **LINESPECIALINFO\_** bit-flag constants describes special information signals that the network can use to report various reporting and network observation operations.</span></span> <span data-ttu-id="30e59-105">Si tratta di sequenze di tono codificate speciali trasmesse all'inizio degli annunci registrati di Network Advisor.</span><span class="sxs-lookup"><span data-stu-id="30e59-105">They are special coded tone sequences transmitted at the beginning of network advisory recorded announcements.</span></span>

<dl> <dt>

<span data-ttu-id="30e59-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**\_CUSTIRREG LINESPECIALINFO**</span><span class="sxs-lookup"><span data-stu-id="30e59-106"><span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO\_CUSTIRREG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="30e59-107">Questo tono speciale di informazioni precede un numero vacante, un AIS, una modifica del numero di Centrex e una stazione non lavorativa, codice di accesso non composto o con connessione in errore o messaggio dell'operatore di intercettazione manuale (categoria di irregolarità del cliente).</span><span class="sxs-lookup"><span data-stu-id="30e59-107">This special information tone precedes a vacant number, AIS, Centrex number change and nonworking station, access code not dialed or dialed in error, or manual intercept operator message (customer irregularity category).</span></span> <span data-ttu-id="30e59-108">LINESPECIALINFO \_ CUSTIRREG viene segnalato anche quando le informazioni di fatturazione vengono rifiutate e quando l'indirizzo composto viene bloccato al commutino.</span><span class="sxs-lookup"><span data-stu-id="30e59-108">LINESPECIALINFO\_CUSTIRREG is also reported when billing information is rejected and when the dialed address is blocked at the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30e59-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuit**</span><span class="sxs-lookup"><span data-stu-id="30e59-109"><span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO\_NOCIRCUIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="30e59-110">Questo tono speciale di informazioni precede un circuito no o un annuncio di emergenza (categoria blocco trunk).</span><span class="sxs-lookup"><span data-stu-id="30e59-110">This special information tone precedes a no circuit or an emergency announcement (trunk blockage category).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30e59-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO \_ Riordina**</span><span class="sxs-lookup"><span data-stu-id="30e59-111"><span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO\_REORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="30e59-112">Questo tono speciale di informazioni precede un annuncio di riordino (categoria di irregolarità delle apparecchiature).</span><span class="sxs-lookup"><span data-stu-id="30e59-112">This special information tone precedes a reorder announcement (equipment irregularity category).</span></span> <span data-ttu-id="30e59-113">\_Il riordino LINESPECIALINFO viene inoltre segnalato quando il telefono viene mantenuto troppo a lungo.</span><span class="sxs-lookup"><span data-stu-id="30e59-113">LINESPECIALINFO\_REORDER is also reported when the telephone is kept offhook too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30e59-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="30e59-114"><span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="30e59-115">Le specifiche relative al tono speciale per le informazioni non sono disponibili e non diventeranno note.</span><span class="sxs-lookup"><span data-stu-id="30e59-115">Specifics about the special information tone are unavailable and will not become known.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="30e59-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="30e59-116"><span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="30e59-117">Le specifiche relative al tono di informazione speciale sono attualmente sconosciute, ma possono essere note in seguito.</span><span class="sxs-lookup"><span data-stu-id="30e59-117">Specifics about the special information tone are currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30e59-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="30e59-118">Remarks</span></span>

<span data-ttu-id="30e59-119">È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30e59-119">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="30e59-120">I 16 bit di ordine inferiore sono riservati.</span><span class="sxs-lookup"><span data-stu-id="30e59-120">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="30e59-121">Per i messaggi consultivi vengono definite note speciali e non vengono in genere utilizzate per scopi di fatturazione o di supervisione.</span><span class="sxs-lookup"><span data-stu-id="30e59-121">Special information tones are defined for advisory messages and are not normally used for billing or supervisory purpose.</span></span>

## <a name="requirements"></a><span data-ttu-id="30e59-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30e59-122">Requirements</span></span>



| <span data-ttu-id="30e59-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e59-123">Requirement</span></span> | <span data-ttu-id="30e59-124">Valore</span><span class="sxs-lookup"><span data-stu-id="30e59-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="30e59-125">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="30e59-125">TAPI version</span></span><br/> | <span data-ttu-id="30e59-126">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="30e59-126">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="30e59-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30e59-127">Header</span></span><br/>       | <dl> <span data-ttu-id="30e59-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="30e59-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




