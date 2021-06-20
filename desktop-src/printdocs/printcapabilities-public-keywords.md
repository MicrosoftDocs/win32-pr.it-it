---
description: Informazioni sugli elementi configurabili dall'utente e sulle definizioni dei parametri che possono essere applicabili a un documento PrintCapabilities.
ms.assetid: 7f08747f-f7ff-4381-b2b9-1917e4708ee3
title: Parole chiave pubbliche di PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d836ca13297f031897598bb2ecbfc6588c49753
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407094"
---
# <a name="printcapabilities-public-keywords"></a><span data-ttu-id="24434-103">Parole chiave pubbliche di PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="24434-103">PrintCapabilities Public Keywords</span></span>

<span data-ttu-id="24434-104">Questo argomento non è corrente.</span><span class="sxs-lookup"><span data-stu-id="24434-104">This topic is not current.</span></span> <span data-ttu-id="24434-105">Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="24434-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="24434-106">La sezione seguente specifica sia gli elementi configurabili dall'utente che le definizioni dei parametri che possono essere applicabili a un documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="24434-106">The following section specifies both user configurable elements and parameter definitions which may be applicable to a PrintCapabilities document.</span></span>

## <a name="user-configurable-elements-usage"></a><span data-ttu-id="24434-107">Utilizzo degli elementi configurabili dall'utente</span><span class="sxs-lookup"><span data-stu-id="24434-107">User Configurable Elements Usage</span></span>

<span data-ttu-id="24434-108">Gli elementi configurabili dall'utente rappresentano parole chiave pubbliche dello schema di stampa che possono essere visualizzate in un documento PrintCapabilities o printTicket.</span><span class="sxs-lookup"><span data-stu-id="24434-108">User Configurable Elements represent Print Schema Public Keywords which may appear in either a PrintCapabilities document or a PrintTicket.</span></span> <span data-ttu-id="24434-109">Sono destinati a rappresentare gli attributi del dispositivo configurabili supportati da un dispositivo specifico o a comunicare la finalità dell'impostazione di stampa da parte di un'applicazione o di un utente.</span><span class="sxs-lookup"><span data-stu-id="24434-109">They are intended to represent configurable device attributes supported by a specific device or communicate print setting intent by an application or user.</span></span>

<span data-ttu-id="24434-110">Gli elementi configurabili dall'utente possono fare riferimento a elementi di riferimento dei parametri.</span><span class="sxs-lookup"><span data-stu-id="24434-110">User Configurable Elements may reference Parameter Reference Elements.</span></span> <span data-ttu-id="24434-111">Per altre informazioni, vedere la sezione [Elementi di riferimento dei](parameter-reference-elements.md) parametri.</span><span class="sxs-lookup"><span data-stu-id="24434-111">For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="parameter-definitions-usage"></a><span data-ttu-id="24434-112">Utilizzo delle definizioni dei parametri</span><span class="sxs-lookup"><span data-stu-id="24434-112">Parameter Definitions Usage</span></span>

<span data-ttu-id="24434-113">Le definizioni dei parametri hanno la forma di tipi di elemento ParameterDef in un documento Di funzionalità di stampa.</span><span class="sxs-lookup"><span data-stu-id="24434-113">Parameters definitions take the form of ParameterDef element types in a Print Capabilities document.</span></span> <span data-ttu-id="24434-114">I tipi di elemento ParameterDef vengono inizializzati in un printticket usando il tipo di elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="24434-114">ParameterDef element types are initialized in a PrintTicket using the ParameterInit element type.</span></span> <span data-ttu-id="24434-115">Il valore del parametro verrà specificato usando l'elemento ParameterInit.</span><span class="sxs-lookup"><span data-stu-id="24434-115">The value of the parameter will be specified using the ParameterInit element.</span></span> <span data-ttu-id="24434-116">Una parola chiave configurabile dall'utente può fare riferimento a una definizione di parametro usando il tipo di elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="24434-116">A user configurable keyword may reference a parameter definition using the ParameterRef element type.</span></span> <span data-ttu-id="24434-117">Per altre informazioni, vedere la [sezione Costrutti di](parameter-constructs.md) parametri.</span><span class="sxs-lookup"><span data-stu-id="24434-117">For more information, please refer to [Parameter Constructs](parameter-constructs.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24434-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24434-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24434-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="24434-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



