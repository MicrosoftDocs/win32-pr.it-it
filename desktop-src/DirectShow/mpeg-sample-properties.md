---
description: Proprietà di esempio MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Proprietà di esempio MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304155"
---
# <a name="mpeg-sample-properties"></a><span data-ttu-id="391b9-103">Proprietà di esempio MPEG</span><span class="sxs-lookup"><span data-stu-id="391b9-103">MPEG Sample Properties</span></span>

<span data-ttu-id="391b9-104">Gli esempi MPEG presentano le seguenti caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="391b9-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="391b9-105">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="391b9-105">**Time Stamps**</span></span>

<span data-ttu-id="391b9-106">Non tutti gli esempi hanno ora di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="391b9-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="391b9-107">L'ora di arresto dell'esempio per i dati del pacchetto e del payload non è utile. viene in genere impostato sull'ora di inizio più uno.</span><span class="sxs-lookup"><span data-stu-id="391b9-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="391b9-108">Per gli esempi di dati del pacchetto o del payload MPEG verrà impostata un'ora di avvio e di arresto se il pacchetto a livello di sistema da cui sono stati generati ha un PTS valido.</span><span class="sxs-lookup"><span data-stu-id="391b9-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="391b9-109">Per ulteriori informazioni sui timestamp, vedere la sezione 2.4.1 di ISO1-11172: "l'intestazione del pacchetto può contenere i timestamp di decodifica e/o di presentazione (DTS e PTS) che fanno riferimento alla prima unità di accesso nel pacchetto".</span><span class="sxs-lookup"><span data-stu-id="391b9-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="391b9-110">Per i \_ tipi principali del flusso MPEG, l'ora di inizio è la posizione in byte del primo byte, valutato a 1 byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="391b9-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="391b9-111">L'ora di arresto è la posizione in byte dell'ultimo byte.</span><span class="sxs-lookup"><span data-stu-id="391b9-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="391b9-112">Pertanto, i campioni consecutivi dovrebbero avere l'ora di arresto del primo pacchetto uguale all'ora di inizio del pacchetto successivo.</span><span class="sxs-lookup"><span data-stu-id="391b9-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="391b9-113">Per i dati del CD video, l'origine del supporto deve corrispondere al formato di un file video CD esposto da CDFS con il blocco RIFF standard all'inizio.</span><span class="sxs-lookup"><span data-stu-id="391b9-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="391b9-114">Per i tipi di payload e pacchetti video MPEG, il timestamp è l'ora di presentazione per il primo fotogramma video il cui codice di avvio dell'immagine inizia nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="391b9-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="391b9-115">Per i tipi di payload e pacchetti audio MPEG, il timestamp è l'ora di presentazione del primo frame audio il cui codice di sincronizzazione inizia nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="391b9-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="391b9-116">Si presuppone che i dati del pacchetto e del payload senza timestamp possano essere registrati correttamente dai filtri di gestione.</span><span class="sxs-lookup"><span data-stu-id="391b9-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="391b9-117">**Discontinuità**</span><span class="sxs-lookup"><span data-stu-id="391b9-117">**Discontinuities**</span></span>

<span data-ttu-id="391b9-118">Se si verifica un'interruzione nel flusso (ad esempio, un gap nei dati in tempo reale o un errore nei dati o dopo una ricerca), la proprietà discontinuità viene impostata sul campione multimediale successivo.</span><span class="sxs-lookup"><span data-stu-id="391b9-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="391b9-119">Ciò consente anche una discontinuità dei timestamp.</span><span class="sxs-lookup"><span data-stu-id="391b9-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="391b9-120">**Notifiche di fine flusso**</span><span class="sxs-lookup"><span data-stu-id="391b9-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="391b9-121">Quando il decodificatore riceve la notifica, deve elaborare i dati memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="391b9-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="391b9-122">Tutti i nuovi dati devono quindi iniziare con la proprietà discontinuità.</span><span class="sxs-lookup"><span data-stu-id="391b9-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="391b9-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="391b9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="391b9-124">Supporto MPEG-2 in DirectShow</span><span class="sxs-lookup"><span data-stu-id="391b9-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



