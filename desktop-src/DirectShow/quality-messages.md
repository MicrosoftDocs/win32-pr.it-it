---
description: Messaggi di qualità
ms.assetid: ff98cb51-6300-470d-b696-5e27591c6b3f
title: Messaggi di qualità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b290833be7550e255590a5bcda449ce19743c0b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521329"
---
# <a name="quality-messages"></a><span data-ttu-id="ef630-103">Messaggi di qualità</span><span class="sxs-lookup"><span data-stu-id="ef630-103">Quality Messages</span></span>

<span data-ttu-id="ef630-104">I messaggi qualitativi vengono definiti con la struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) .</span><span class="sxs-lookup"><span data-stu-id="ef630-104">Quality messages are defined with the [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure.</span></span> <span data-ttu-id="ef630-105">Questa struttura contiene i membri seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef630-105">This structure contains the following members:</span></span>

-   <span data-ttu-id="ef630-106">**Tipo:** Definito dall'enumerazione [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) . entrambe le carestie, a indicare che il filtro sta ricevendo dati troppo piccoli o flood, a indicare che il filtro sta ricevendo troppi dati.</span><span class="sxs-lookup"><span data-stu-id="ef630-106">**Type:** Defined by the [**QualityMessageType**](/windows/win32/api/strmif/ne-strmif-qualitymessagetype) enumeration; either Famine, indicating that the filter is receiving too little data, or Flood, indicating that the filter is receiving too much data.</span></span>
-   <span data-ttu-id="ef630-107">**Proporzione:** Regolazione richiesta nella velocità dati, da una linea di base 1000.</span><span class="sxs-lookup"><span data-stu-id="ef630-107">**Proportion:** The requested adjustment in the data rate, from a baseline of 1000.</span></span> <span data-ttu-id="ef630-108">750 indica, ad esempio, 75% e 1500 indica il 150%.</span><span class="sxs-lookup"><span data-stu-id="ef630-108">For example, 750 indicates 75% and 1500 indicates 150%.</span></span>
-   <span data-ttu-id="ef630-109">In **ritardo:** Tempo di riferimento che indica la fine dell'arrivo dell'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="ef630-109">**Late:** Reference time indicating how late the most recent sample arrived.</span></span> <span data-ttu-id="ef630-110">Il valore è negativo se l'esempio è arrivato in anticipo.</span><span class="sxs-lookup"><span data-stu-id="ef630-110">The value is negative if the sample arrived early.</span></span>
-   <span data-ttu-id="ef630-111">**Timestamp:** Timestamp dell'esempio più recente.</span><span class="sxs-lookup"><span data-stu-id="ef630-111">**TimeStamp:** The time stamp on the most recent sample.</span></span>

<span data-ttu-id="ef630-112">Si supponga, ad esempio, che un campione con un timestamp di 240 millisecondi (MS) raggiunga il renderer a 280 MS, il flusso di tempo.</span><span class="sxs-lookup"><span data-stu-id="ef630-112">For example, suppose that a sample with a time stamp of 240 milliseconds (ms) reaches the renderer at 280 ms, stream time.</span></span> <span data-ttu-id="ef630-113">Il renderer crea un messaggio qualitativo di tipo carestie.</span><span class="sxs-lookup"><span data-stu-id="ef630-113">The renderer creates a quality message of type Famine.</span></span> <span data-ttu-id="ef630-114">L'esempio è arrivato 40 ms tardi, quindi il membro **tardivo** è 400000.</span><span class="sxs-lookup"><span data-stu-id="ef630-114">The sample arrived 40 ms late, so the **Late** member is 400000.</span></span> <span data-ttu-id="ef630-115">(Tutti i tempi di riferimento sono in unità di 100 nanosecondi). Il membro **timestamp** è 2,4 milioni.</span><span class="sxs-lookup"><span data-stu-id="ef630-115">(All reference times are in 100-nanosecond units.) The **TimeStamp** member is 2400000.</span></span>

<span data-ttu-id="ef630-116">Per il membro **proporzionale** , il renderer può utilizzare una media in esecuzione per calcolare il valore.</span><span class="sxs-lookup"><span data-stu-id="ef630-116">For the **Proportion** member, the renderer might use a running average to calculate the value.</span></span> <span data-ttu-id="ef630-117">Forse gli esempi sono arrivati in tempo e questo esempio è un'anomalia.</span><span class="sxs-lookup"><span data-stu-id="ef630-117">Perhaps samples have been arriving on time, and this sample is an anomaly.</span></span> <span data-ttu-id="ef630-118">In tal caso, il renderer potrebbe richiedere solo una piccola correzione.</span><span class="sxs-lookup"><span data-stu-id="ef630-118">In that case the renderer might request only a small correction.</span></span> <span data-ttu-id="ef630-119">D'altra parte, se gli esempi sono costantemente tardi, il renderer potrebbe richiedere una correzione più grande.</span><span class="sxs-lookup"><span data-stu-id="ef630-119">On the other hand, if samples are consistently late, the renderer might request a larger correction.</span></span>

<span data-ttu-id="ef630-120">Il controllo qualità viene gestito tramite l'interfaccia [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="ef630-120">Quality control is handled through the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) interface.</span></span> <span data-ttu-id="ef630-121">Contiene due metodi.</span><span class="sxs-lookup"><span data-stu-id="ef630-121">It contains two methods.</span></span>

-   <span data-ttu-id="ef630-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Invia un messaggio di qualità.</span><span class="sxs-lookup"><span data-stu-id="ef630-122">[**Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify): Sends a quality message.</span></span>
-   <span data-ttu-id="ef630-123">[**SESINK**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): specifica un gestore qualità personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ef630-123">[**SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink): Specifies a custom quality manager.</span></span>

<span data-ttu-id="ef630-124">Un oggetto che implementa **IQualityControl** riceve messaggi di qualità tramite il metodo **Notify** .</span><span class="sxs-lookup"><span data-stu-id="ef630-124">An object that implements **IQualityControl** receives quality messages through its **Notify** method.</span></span> <span data-ttu-id="ef630-125">Il messaggio può essere gestito o passato a un altro oggetto.</span><span class="sxs-lookup"><span data-stu-id="ef630-125">It can either handle the message or pass the message to another object.</span></span> <span data-ttu-id="ef630-126">Se l'applicazione chiama **il metodo SetValue dell'oggetto** , l'oggetto deve delegare il controllo qualità al gestore qualità specificato.</span><span class="sxs-lookup"><span data-stu-id="ef630-126">If the application calls the object's **SetSink** method, the object should delegate quality control to the specified quality manager.</span></span>

 

 



