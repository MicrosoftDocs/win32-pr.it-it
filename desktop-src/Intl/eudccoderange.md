---
description: La chiave del Registro di sistema EUDCCodeRange definisce intervalli di codice di caratteri definiti dall'utente finale (EUDC) per diverse code pages (set di caratteri).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619bce02f4ca66fa9b4ce6d25aff0c5a3e66f96
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120676"
---
# <a name="eudccoderange"></a><span data-ttu-id="3334b-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="3334b-103">EUDCCodeRange</span></span>

<span data-ttu-id="3334b-104">La chiave del Registro di sistema EUDCCodeRange definisce intervalli di codice di caratteri definiti dall'utente [finale (EUDC)](end-user-defined-characters.md) per diverse code pages (set di caratteri).</span><span class="sxs-lookup"><span data-stu-id="3334b-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="3334b-105">Viene usato solo dagli strumenti che creano UDC e non è di interesse diretto per gli utenti di EUDC.</span><span class="sxs-lookup"><span data-stu-id="3334b-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="3334b-106">Questa chiave del Registro di sistema ha il percorso del Registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="3334b-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="3334b-107">HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ NLS \\ CodePage \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="3334b-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="3334b-108">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="3334b-108">The format is:</span></span>

<span data-ttu-id="3334b-109">EUDCCodeRange CodePage=FromTo \[ ,FromTo\]</span><span class="sxs-lookup"><span data-stu-id="3334b-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="3334b-110">dove:</span><span class="sxs-lookup"><span data-stu-id="3334b-110">where:</span></span>



| <span data-ttu-id="3334b-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3334b-111">Value</span></span>         | <span data-ttu-id="3334b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3334b-112">Description</span></span>                                                                                                                                                                                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3334b-113">CodePage</span><span class="sxs-lookup"><span data-stu-id="3334b-113">CodePage</span></span> | <span data-ttu-id="3334b-114">Una delle stringhe "932" (giapponese), "936" (cinese semplificato), "949" (coreano), "950" (cinese tradizionale) o "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="3334b-114">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="3334b-115">Non sono supportati altri valori.</span><span class="sxs-lookup"><span data-stu-id="3334b-115">No other values are supported.</span></span>                                     |
| <span data-ttu-id="3334b-116">FromTo</span><span class="sxs-lookup"><span data-stu-id="3334b-116">FromTo</span></span>   | <span data-ttu-id="3334b-117">Valore stringa costituito da una coppia di valori esadecimali a 4 cifre separati da un trattino (-).</span><span class="sxs-lookup"><span data-stu-id="3334b-117">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="3334b-118">È possibile specificare fino a quattro valori FromTo, ognuno dei quali deve essere separato dal valore precedente da una virgola (,).</span><span class="sxs-lookup"><span data-stu-id="3334b-118">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="3334b-119">Di seguito sono riportati i valori corretti per la voce del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3334b-119">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="3334b-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3334b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3334b-121">Voci del Registro di sistema EUDC</span><span class="sxs-lookup"><span data-stu-id="3334b-121">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="3334b-122">Eudc</span><span class="sxs-lookup"><span data-stu-id="3334b-122">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



