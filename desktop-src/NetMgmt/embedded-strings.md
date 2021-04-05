---
title: Stringhe incorporate
description: Le strutture informative non conterranno stringhe incorporate. Ciò migliora l'allineamento delle strutture di informazioni e consente la flessibilità OEM nelle funzioni di base.
ms.assetid: a3272a0a-5352-4847-84fd-113b4467c32c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c71ed50971661f9ad06855024ecba2796f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711578"
---
# <a name="embedded-strings"></a><span data-ttu-id="301b4-104">Stringhe incorporate</span><span class="sxs-lookup"><span data-stu-id="301b4-104">Embedded Strings</span></span>

<span data-ttu-id="301b4-105">Le strutture informative non conterranno stringhe incorporate.</span><span class="sxs-lookup"><span data-stu-id="301b4-105">Information structures will not contain embedded strings.</span></span> <span data-ttu-id="301b4-106">Ciò migliora l'allineamento delle strutture di informazioni e consente la flessibilità OEM nelle funzioni di base.</span><span class="sxs-lookup"><span data-stu-id="301b4-106">This improves the alignment of the information structures and allows for OEM flexibility in the core functions.</span></span>

<span data-ttu-id="301b4-107">Qualsiasi campo informazioni restituito in una chiamata di enumerazione che può essere successivamente usato come chiave per la chiamata a una funzione di gestione di rete GetInfo è sicuramente presente nel buffer di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="301b4-107">Any information field that is returned in an enumeration call that can be subsequently used as a key for the call to a GetInfo network management function is guaranteed to be present in the enumeration buffer.</span></span> <span data-ttu-id="301b4-108">Se la stringa di informazioni a lunghezza variabile che specifica il valore del campo chiave non si adatta, non viene restituita l'intera struttura a lunghezza fissa per la voce.</span><span class="sxs-lookup"><span data-stu-id="301b4-108">If the variable-length information string that would specify the key field value will not fit, then the entire fixed-length structure for the entry is not returned.</span></span> <span data-ttu-id="301b4-109">Altri campi a lunghezza variabile verranno restituiti come puntatore **null** per il caso in cui la stringa non è adatta.</span><span class="sxs-lookup"><span data-stu-id="301b4-109">Other variable-length fields will be returned as a **NULL** pointer for the case in which the string does not fit.</span></span>

 

 




