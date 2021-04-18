---
description: La chiave del registro di sistema EUDCCodeRange definisce gli intervalli di codice dei caratteri definiti dall'utente finale (EUDC) per varie tabelle codici (set di caratteri).
ms.assetid: 11a167a0-f2a3-4b8b-a38c-70cf14c895be
title: EUDCCodeRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e68c71751ca5d13cd04c95ff66c84067fd1d46d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317151"
---
# <a name="eudccoderange"></a><span data-ttu-id="49149-103">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="49149-103">EUDCCodeRange</span></span>

<span data-ttu-id="49149-104">La chiave del registro di sistema EUDCCodeRange definisce gli intervalli di codice dei [caratteri definiti dall'utente finale (EUDC)](end-user-defined-characters.md) per varie tabelle codici (set di caratteri).</span><span class="sxs-lookup"><span data-stu-id="49149-104">The EUDCCodeRange registry key defines [end-user-defined character (EUDC)](end-user-defined-characters.md) code ranges for various code pages (character sets).</span></span> <span data-ttu-id="49149-105">Viene usato solo da strumenti che creano EUDCs e non è un problema diretto per gli utenti di EUDC.</span><span class="sxs-lookup"><span data-stu-id="49149-105">It is used only by tools that create EUDCs, and is not of direct concern to EUDC users.</span></span> <span data-ttu-id="49149-106">Questa chiave del registro di sistema presenta il seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="49149-106">This registry key has the following registry location:</span></span>

<span data-ttu-id="49149-107">HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ controllo \\ NLS tabella \\ codici \\ EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="49149-107">HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\NLS\\CodePage\\EUDCCodeRange</span></span>

<span data-ttu-id="49149-108">Il formato è:</span><span class="sxs-lookup"><span data-stu-id="49149-108">The format is:</span></span>

<span data-ttu-id="49149-109">Tabella codici EUDCCodeRange = FromTo \[ , FromTo\]</span><span class="sxs-lookup"><span data-stu-id="49149-109">EUDCCodeRange CodePage=FromTo\[,FromTo\]</span></span>

<span data-ttu-id="49149-110">dove:</span><span class="sxs-lookup"><span data-stu-id="49149-110">where:</span></span>



|          |                                                                                                                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49149-111">CodePage</span><span class="sxs-lookup"><span data-stu-id="49149-111">CodePage</span></span> | <span data-ttu-id="49149-112">Una delle stringhe "932" (giapponese), "936" (cinese semplificato), "949" (coreano), "950" (cinese tradizionale) o "Unicode" (Unicode).</span><span class="sxs-lookup"><span data-stu-id="49149-112">One of the strings "932" (Japanese), "936" (Simplified Chinese), "949" (Korean), "950" (Traditional Chinese), or "Unicode" (Unicode).</span></span> <span data-ttu-id="49149-113">Nessun altro valore supportato.</span><span class="sxs-lookup"><span data-stu-id="49149-113">No other values are supported.</span></span>                                     |
| <span data-ttu-id="49149-114">FromTo</span><span class="sxs-lookup"><span data-stu-id="49149-114">FromTo</span></span>   | <span data-ttu-id="49149-115">Valore stringa costituito da una coppia di valori esadecimali a 4 cifre separati da un trattino (-).</span><span class="sxs-lookup"><span data-stu-id="49149-115">String value consisting of a pair of 4-digit hexadecimal values separated by a hyphen (-).</span></span> <span data-ttu-id="49149-116">È possibile specificare fino a quattro valori FromTo, ognuno dei quali deve essere separato dal valore precedente mediante una virgola (,).</span><span class="sxs-lookup"><span data-stu-id="49149-116">Up to four FromTo values can be specified, but each must be separated from the previous value by a comma (,).</span></span> |



 

<span data-ttu-id="49149-117">Di seguito sono riportati i valori corretti per la voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="49149-117">The following are the correct values for the registry entry.</span></span>


```C++
932=F040-F9FC
936=A140-A7A0,AAA1-AFFE,F8A1-FEFE
949=C9A1-C9FE,FEA1-FEFE
950=8140-8DFE,8E40-A0FE,C6A1-C8FE,FA40-FEFE
Unicode=E000-F8FF
```



## <a name="related-topics"></a><span data-ttu-id="49149-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49149-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49149-119">Voci del registro di sistema EUDC</span><span class="sxs-lookup"><span data-stu-id="49149-119">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="49149-120">EUDC</span><span class="sxs-lookup"><span data-stu-id="49149-120">EUDC</span></span>](eudc.md)
</dt> </dl>

 

 



