---
description: I tipi di formato chiave dei dati configurabili possono essere utilizzati nei campi di testo per fornire una chiave in una tabella di database.
ms.assetid: 9f3ce218-1243-4eba-9866-113200fefa30
title: Tipi di formato chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96687299a57ddebbb90b422ad5311c4bed1db332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307257"
---
# <a name="key-format-types"></a><span data-ttu-id="a3553-103">Tipi di formato chiave</span><span class="sxs-lookup"><span data-stu-id="a3553-103">Key Format Types</span></span>

<span data-ttu-id="a3553-104">I tipi di formato chiave dei dati configurabili possono essere utilizzati nei campi di testo per fornire una chiave in una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="a3553-104">The Key Format Types of configurable data may be used in text fields to provide a key into a database table.</span></span> <span data-ttu-id="a3553-105">L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo.</span><span class="sxs-lookup"><span data-stu-id="a3553-105">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="a3553-106">Null non è mai un valore valido per questo tipo.</span><span class="sxs-lookup"><span data-stu-id="a3553-106">Null is never a valid value for this type.</span></span> <span data-ttu-id="a3553-107">Le risposte a tutti gli elementi di formato chiave devono essere nel [formato speciale CMSM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="a3553-107">Responses to all Key format items must be in [CMSM Special Format](cmsm-special-format.md).</span></span>

<span data-ttu-id="a3553-108">Esistono i tipi di formato chiave seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3553-108">The following Key Format types exist:</span></span>

[<span data-ttu-id="a3553-109">Tipo di directory</span><span class="sxs-lookup"><span data-stu-id="a3553-109">Directory Type</span></span>](directory-type.md)

[<span data-ttu-id="a3553-110">Tipo di file</span><span class="sxs-lookup"><span data-stu-id="a3553-110">File Type</span></span>](file-type.md)

[<span data-ttu-id="a3553-111">Tipo di proprietà</span><span class="sxs-lookup"><span data-stu-id="a3553-111">Property Type</span></span>](property-type.md)

[<span data-ttu-id="a3553-112">Tipo di finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="a3553-112">Dialog Type</span></span>](dialog-type.md)

[<span data-ttu-id="a3553-113">Tipo binario</span><span class="sxs-lookup"><span data-stu-id="a3553-113">Binary Type</span></span>](binary-type.md)

[<span data-ttu-id="a3553-114">Tipo di icona</span><span class="sxs-lookup"><span data-stu-id="a3553-114">Icon Type</span></span>](icon-type.md)

<span data-ttu-id="a3553-115">Gli elementi configurabili del tipo di formato chiave vengono utilizzati nelle colonne di testo per fornire una chiave del database e, in generale, possono essere sostituiti da qualsiasi stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="a3553-115">Configurable items of the Key Format Type are used in text columns to provide a database key and in general could be replaced by any text string.</span></span> <span data-ttu-id="a3553-116">I singoli tipi possono avere restrizioni sintattiche aggiuntive, ma queste restrizioni non vengono applicate da Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="a3553-116">The individual types may have additional syntactic restrictions, but these restrictions are not enforced by Mergemod.dll.</span></span> <span data-ttu-id="a3553-117">Particolari elementi configurabili possono anche avere restrizioni semantiche caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="a3553-117">Particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="a3553-118">Ad esempio, potrebbe essere necessario un particolare elemento configurabile come chiave nella [tabella binaria](binary-table.md) in una riga contenente un'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="a3553-118">For example, a particular configurable item may be required to be a key into the [Binary table](binary-table.md) to a row containing a bitmap image.</span></span> <span data-ttu-id="a3553-119">Tali restrizioni non vengono applicate da Mergemod.dll e pertanto gli autori dei moduli devono essere preparati a gestire qualsiasi stringa che soddisfi il tipo di formato della chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="a3553-119">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Key Format type.</span></span> <span data-ttu-id="a3553-120">Se non diversamente specificato dal significato semantico o dagli attributi, null è una risposta valida.</span><span class="sxs-lookup"><span data-stu-id="a3553-120">Unless otherwise specified by semantic meaning or attributes, null is a valid response.</span></span>

 

 



