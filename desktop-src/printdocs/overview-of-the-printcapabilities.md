---
description: PrintCapabilities descrive le configurazioni o gli stati disponibili in un dispositivo, che spesso possono essere inseriti in diverse configurazioni.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Panoramica di PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8f61d1ee4125a9a1ac5f9ddb07cf226cd7094e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408524"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="c91ff-103">Panoramica di PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c91ff-103">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="c91ff-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="c91ff-104">This topic is not current.</span></span> <span data-ttu-id="c91ff-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c91ff-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c91ff-106">PrintCapabilities descrive le configurazioni o gli stati disponibili in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c91ff-106">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="c91ff-107">Un dispositivo descritto da PrintCapabilities può spesso essere inserito in diverse configurazioni.</span><span class="sxs-lookup"><span data-stu-id="c91ff-107">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="c91ff-108">Nel caso di un dispositivo di stampa, gli attributi di stampa tipici includono la stampa duplex, la risoluzione e le dimensioni dei supporti.</span><span class="sxs-lookup"><span data-stu-id="c91ff-108">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="c91ff-109">Se il dispositivo supporta questi attributi, fanno parte della configurazione per tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c91ff-109">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="c91ff-110">L'utente seleziona una particolare configurazione assegnando un valore specifico a ognuno degli attributi disponibili. ad esempio Duplex: OneSided, Resolution: 600 dpi e MediaSize: Legal.</span><span class="sxs-lookup"><span data-stu-id="c91ff-110">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="c91ff-111">PrintCapabilities si basa su Print Schema Framework, che definisce gli elementi che possono essere usati in PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c91ff-111">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="c91ff-112">Le parole chiave dello schema di stampa definiscono gerarchie di elementi di uso comune, o parole chiave, allo scopo di promuovere la portabilità delle informazioni e della finalità tra i singoli client.</span><span class="sxs-lookup"><span data-stu-id="c91ff-112">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="c91ff-113">Tuttavia, le parole chiave dello schema di stampa consentono anche estensioni private in modo che PrintCapabilities possa essere personalizzato per soddisfare esigenze specifiche.</span><span class="sxs-lookup"><span data-stu-id="c91ff-113">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c91ff-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c91ff-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c91ff-115">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="c91ff-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



