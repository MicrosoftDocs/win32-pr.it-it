---
description: Informazioni sui parametri nel documento PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: d317d052-c207-412a-896e-09cb57b0dd5f
title: Parametri nel documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6b2ba61f1985fdcd02f40e8e08100725968a8e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118626"
---
# <a name="parameters-in-the-printcapabilities-document"></a><span data-ttu-id="1680f-105">Parametri nel documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="1680f-105">Parameters in the PrintCapabilities Document</span></span>

<span data-ttu-id="1680f-106">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="1680f-106">This topic is not current.</span></span> <span data-ttu-id="1680f-107">Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1680f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1680f-108">Come illustrato in [Elementi di riferimento](parameter-reference-elements.md)ai parametri, è possibile fare riferimento agli elementi ParameterInit dall'interno di istanze Option, ma anche il costrutto di parametro ha un uso indipendente da questo tipo di elemento.</span><span class="sxs-lookup"><span data-stu-id="1680f-108">As discussed in [Parameter Reference Elements](parameter-reference-elements.md), ParameterInit elements may be referenced from within Option instances, but the parameter construct also has a use that is independent of this type of element.</span></span>

<span data-ttu-id="1680f-109">Un esempio di attributo di configurazione del dispositivo adatto per la rappresentazione dei parametri è CopyCount.</span><span class="sxs-lookup"><span data-stu-id="1680f-109">An example of a device configuration attribute that is well suited for parameter representation is CopyCount.</span></span> <span data-ttu-id="1680f-110">I valori consentiti per questo attributo di configurazione del dispositivo possono essere definiti in modo semplice e conciso senza elencarli in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1680f-110">The allowed values for this device configuration attribute can be easily and concisely defined without listing each of them explicitly.</span></span> <span data-ttu-id="1680f-111">Anche se sarebbe possibile, anche se noioso, elencare ogni valore CopyCount nella propria opzione, alcuni attributi di configurazione del dispositivo semplicemente non possono essere rappresentati usando un costrutto Feature/Option.</span><span class="sxs-lookup"><span data-stu-id="1680f-111">Although it would be possible, though tedious, to list each CopyCount value in its own Option, some device configuration attributes simply cannot be represented using a Feature/Option construct.</span></span> <span data-ttu-id="1680f-112">Si consideri ad esempio un dispositivo che accetta una stringa di testo che viene quindi usata per produrre una filigrana virtuale in ogni pagina di output.</span><span class="sxs-lookup"><span data-stu-id="1680f-112">As an example, consider a device that accepts a text string that is then used to produce a virtual watermark on each output page.</span></span> <span data-ttu-id="1680f-113">Il set di tutte le stringhe di testo possibili non può essere enumerato in modo esplicito, ma la stringa di testo può essere descritta facilmente usando un elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="1680f-113">The set of all possible text strings cannot easily be explicitly enumerated, but the text string can easily be described using a ParameterDef element.</span></span>

<span data-ttu-id="1680f-114">Il documento Parole chiave dello schema di stampa definisce una serie di costrutti di parametro di uso comune, ma i provider PrintCapabilities sono liberi di definire altri costrutti personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1680f-114">The Print Schema Keywords document defines a number of commonly used parameter constructs, but PrintCapabilities providers are free to define additional ones of their own.</span></span> <span data-ttu-id="1680f-115">Tuttavia, questi costrutti di parametro definiti privatamente non sono portabili per altri dispositivi, a causa del fatto che un documento PrintCapabilities fornito da un'altra parte non definisce tale costrutto di parametro.</span><span class="sxs-lookup"><span data-stu-id="1680f-115">However, these privately-defined parameter constructs are not portable to other devices, due to the fact that a PrintCapabilities document provided by another party does not define such a parameter construct.</span></span> <span data-ttu-id="1680f-116">Indipendentemente dal fatto che sia definita dallo schema o privata, l'istanza ParameterDef deve essere presente nel documento PrintCapabilities prima che il parametro venga riconosciuto e usato dai client.</span><span class="sxs-lookup"><span data-stu-id="1680f-116">Whether schema-defined or privately-defined, the ParameterDef instance must be present in the PrintCapabilities document before the parameter is recognized and used by clients.</span></span> <span data-ttu-id="1680f-117">Questi parametri sono definiti *parametri designati.*</span><span class="sxs-lookup"><span data-stu-id="1680f-117">These parameters are referred to as *designated parameters*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1680f-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1680f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1680f-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="1680f-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



