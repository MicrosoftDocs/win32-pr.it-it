---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parametri nel documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ecfcfee581014bdb57ff70adebaf5f4c8b6fedc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351831"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="fc893-104">Parametri nel documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="fc893-104">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="fc893-105">Questo argomento non è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="fc893-105">This topic is not current.</span></span> <span data-ttu-id="fc893-106">Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fc893-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fc893-107">Come illustrato negli [elementi di riferimento ai parametri](parameter-reference-elements.md), è possibile fare riferimento agli elementi ParameterInit all'interno di istanze di opzioni, ma anche il costrutto di parametro ha un uso indipendente da questo tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="fc893-107">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="fc893-108">Un esempio di attributo di configurazione del dispositivo particolarmente adatto per la rappresentazione del parametro è CopyCount.</span><span class="sxs-lookup"><span data-stu-id="fc893-108">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="fc893-109">I valori consentiti per questo attributo di configurazione del dispositivo possono essere definiti in modo semplice e conciso senza elencarli singolarmente.</span><span class="sxs-lookup"><span data-stu-id="fc893-109">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="fc893-110">Sebbene sarebbe possibile, sebbene noioso, elencare ogni valore CopyCount nella propria opzione, alcuni attributi di configurazione del dispositivo semplicemente non possono essere rappresentati usando un costrutto di funzionalità o opzione.</span><span class="sxs-lookup"><span data-stu-id="fc893-110">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="fc893-111">Ad esempio, si consideri un dispositivo che accetta una stringa di testo che viene quindi usata per produrre una filigrana virtuale in ogni pagina di output.</span><span class="sxs-lookup"><span data-stu-id="fc893-111">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="fc893-112">Il set di tutte le stringhe di testo possibili non può essere facilmente enumerato in modo esplicito, ma la stringa di testo può essere facilmente descritta utilizzando un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="fc893-112">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="fc893-113">Il documento parole chiave dello schema di stampa definisce un numero di costrutti di parametri comunemente utilizzati, ma i provider PrintCapabilities sono liberi di definire quelli più comuni.</span><span class="sxs-lookup"><span data-stu-id="fc893-113">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="fc893-114">Tuttavia, questi costrutti di parametro definiti privatamente non sono portabili ad altri dispositivi, a causa del fatto che un documento PrintCapabilities fornito da un'altra parte non definisce tale costrutto di parametro.</span><span class="sxs-lookup"><span data-stu-id="fc893-114">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="fc893-115">Se definito dallo schema o privato, l'istanza di ParameterDef deve essere presente nel documento PrintCapabilities prima che il parametro venga riconosciuto e utilizzato dai client.</span><span class="sxs-lookup"><span data-stu-id="fc893-115">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="fc893-116">Questi parametri sono detti *parametri designati*.</span><span class="sxs-lookup"><span data-stu-id="fc893-116">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc893-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fc893-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc893-118">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="fc893-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



