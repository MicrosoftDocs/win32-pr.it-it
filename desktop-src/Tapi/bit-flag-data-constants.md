---
description: Per le costanti di dati dei flag di bit estendibili, un fornitore del provider di servizi può definire nuovi valori per i bit specificati.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Costanti dati Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309975"
---
# <a name="bit-flag-data-constants"></a><span data-ttu-id="23c51-103">Costanti dati Bit-Flag</span><span class="sxs-lookup"><span data-stu-id="23c51-103">Bit-Flag Data Constants</span></span>

<span data-ttu-id="23c51-104">Per le costanti di dati dei flag di bit estendibili, un fornitore del provider di servizi può definire nuovi valori per i bit specificati.</span><span class="sxs-lookup"><span data-stu-id="23c51-104">For extensible bit-flag data constants, a service-provider vendor can define new values for specified bits.</span></span> <span data-ttu-id="23c51-105">Poiché la maggior parte delle costanti di flag di bit è **DWORD** s, un numero specifico di bit inferiori è generalmente riservato per le estensioni comuni, mentre i bit superiori rimanenti sono disponibili per le estensioni specifiche del fornitore.</span><span class="sxs-lookup"><span data-stu-id="23c51-105">Because most bit-flag constants are **DWORD** s, a specific number of the lower bits are usually reserved for common extensions, while the remaining upper bits are available for vendor-specific extensions.</span></span> <span data-ttu-id="23c51-106">I flag di bit comuni sono assegnati dal bit zero e le estensioni specifiche del fornitore devono essere assegnate dal bit 31 verso il basso.</span><span class="sxs-lookup"><span data-stu-id="23c51-106">Common bit flags are assigned from bit zero up, and vendor-specific extensions should be assigned from bit 31 down.</span></span> <span data-ttu-id="23c51-107">Questo schema offre la massima flessibilità nell'assegnazione di posizioni di bit a estensioni comuni, anziché estensioni specifiche del fornitore.</span><span class="sxs-lookup"><span data-stu-id="23c51-107">This scheme provides maximum flexibility in assigning bit positions to common extensions, as opposed to vendor-specific extensions.</span></span> <span data-ttu-id="23c51-108">Si prevede che un fornitore definisca nuovi valori che sono estensioni naturali dei flag di bit definiti dall'API.</span><span class="sxs-lookup"><span data-stu-id="23c51-108">A vendor is expected to define new values that are natural extensions of the bit flags defined by the API.</span></span>

<span data-ttu-id="23c51-109">Le strutture di dati estendibili hanno un campo di dimensioni sempre più riservato per l'uso specifico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="23c51-109">Extensible data structures have a variably sized field that is reserved for device-specific use.</span></span> <span data-ttu-id="23c51-110">Poiché il campo è di dimensioni variabili, il provider di servizi decide la quantità di informazioni e l'interpretazione del campo.</span><span class="sxs-lookup"><span data-stu-id="23c51-110">Because the field is variably sized, the service provider decides the field's amount of information and interpretation.</span></span> <span data-ttu-id="23c51-111">Si prevede che un fornitore che definisce un campo specifico del dispositivo renda le estensioni naturali della struttura di dati originale definita dall'API.</span><span class="sxs-lookup"><span data-stu-id="23c51-111">A vendor that defines a device-specific field is expected to make these natural extensions of the original data structure defined by the API.</span></span>

 

 



