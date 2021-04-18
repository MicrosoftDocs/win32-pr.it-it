---
description: Impostazione della velocità di riproduzione
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Impostazione della velocità di riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303692"
---
# <a name="setting-the-playback-rate"></a><span data-ttu-id="a6291-103">Impostazione della velocità di riproduzione</span><span class="sxs-lookup"><span data-stu-id="a6291-103">Setting the Playback Rate</span></span>

<span data-ttu-id="a6291-104">Per modificare la velocità di riproduzione, chiamare il metodo [**IMediaSeeking:: serate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="a6291-104">To change the playback rate, call the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span> <span data-ttu-id="a6291-105">Specificare la nuova velocità come frazione della frequenza originale.</span><span class="sxs-lookup"><span data-stu-id="a6291-105">Specify the new rate as a fraction of the original rate.</span></span> <span data-ttu-id="a6291-106">Per riprodurre, ad esempio, una velocità di due volte normale, utilizzare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="a6291-106">For example, to play at twice-normal speed, use the following:</span></span>


```C++
pSeek->SetRate(2.0)
```



<span data-ttu-id="a6291-107">Le tariffe maggiori di uno sono più veloci del normale.</span><span class="sxs-lookup"><span data-stu-id="a6291-107">Rates greater than one are faster than normal.</span></span> <span data-ttu-id="a6291-108">Le tariffe comprese tra zero e uno sono inferiori al normale.</span><span class="sxs-lookup"><span data-stu-id="a6291-108">Rates between zero and one are slower than normal.</span></span> <span data-ttu-id="a6291-109">Le frequenze negative sono definite come riproduzione indietro, ma in pratica la maggior parte dei filtri non le supporta.</span><span class="sxs-lookup"><span data-stu-id="a6291-109">Negative rates are defined as backward playback, but in practice most filters do not support it.</span></span> <span data-ttu-id="a6291-110">Attualmente nessuno dei filtri DirectShow standard supporta la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="a6291-110">Currently none of the standard DirectShow filters support reverse playback.</span></span>

<span data-ttu-id="a6291-111">Indipendentemente dalla velocità di riproduzione, la posizione corrente e la posizione di arresto sono sempre espresse in relazione all'origine originale.</span><span class="sxs-lookup"><span data-stu-id="a6291-111">Regardless of the playback rate, the current position and the stop position are always expressed relative to the original source.</span></span> <span data-ttu-id="a6291-112">Se, ad esempio, un file di origine è di 20 secondi alla frequenza di riproduzione normale, se si imposta la posizione corrente su 10 secondi verrà cercata al centro del file.</span><span class="sxs-lookup"><span data-stu-id="a6291-112">For example, if a source file is 20 seconds long at normal playback rate, setting the current position to 10 seconds will seek to the middle of the file.</span></span> <span data-ttu-id="a6291-113">Se la frequenza di riproduzione è 2,0, la posizione di arresto è 20 secondi e si cerca la posizione di 10 secondi, il file verrà riprodotto per 5 secondi di tempo reale: 10 secondi, con una doppia velocità di riproduzione normale.</span><span class="sxs-lookup"><span data-stu-id="a6291-113">If the playback rate is 2.0, the stop position is 20 seconds, and you seek to the 10-second position, the file will play for 5 seconds of real time: 10 seconds' worth, at twice the normal playback speed.</span></span> <span data-ttu-id="a6291-114">Con la velocità di riproduzione 2,0, la posizione corrente aumenta al doppio della frequenza del clock di riferimento.</span><span class="sxs-lookup"><span data-stu-id="a6291-114">At a playback rate of 2.0, the current position increases at twice the rate of the reference clock.</span></span>

 

 



