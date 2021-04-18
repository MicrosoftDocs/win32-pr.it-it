---
description: Questo attributo misura la distanza di riempimento della barra indicatore di stato.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Attributo di controllo progress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318651"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="b87f5-103">Attributo di controllo progress</span><span class="sxs-lookup"><span data-stu-id="b87f5-103">Progress Control Attribute</span></span>

<span data-ttu-id="b87f5-104">Questo attributo misura la distanza di riempimento della barra indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="b87f5-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="b87f5-105">Il record contiene due Integer e una stringa.</span><span class="sxs-lookup"><span data-stu-id="b87f5-105">The record contains two integers and a string.</span></span> <span data-ttu-id="b87f5-106">Il primo numero è lo stato di avanzamento, il secondo numero è l'intervallo (il numero massimo possibile per lo stato di avanzamento).</span><span class="sxs-lookup"><span data-stu-id="b87f5-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="b87f5-107">In impostazione, i numeri interi possono essere immessi come campi interi o stringhe contenenti i numeri interi.</span><span class="sxs-lookup"><span data-stu-id="b87f5-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="b87f5-108">Se il secondo numero è mancante, si presuppone che sia il valore predefinito (1024).</span><span class="sxs-lookup"><span data-stu-id="b87f5-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="b87f5-109">Se lo stato di avanzamento è maggiore di quello dell'intervallo, questo viene modificato in modo da essere compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="b87f5-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="b87f5-110">Il terzo campo è una stringa, il nome dell'azione di cui viene visualizzato lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b87f5-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="b87f5-111">Per informazioni correlate, vedere [creazione di un controllo ProgressBar](authoring-a-progressbar-control.md)e [aggiunta di azioni personalizzate a ProgressBar](adding-custom-actions-to-the-progressbar.md).</span><span class="sxs-lookup"><span data-stu-id="b87f5-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="b87f5-112">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="b87f5-112">Valid Controls</span></span>

[<span data-ttu-id="b87f5-113">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="b87f5-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="b87f5-114">Flag di bit associati</span><span class="sxs-lookup"><span data-stu-id="b87f5-114">Associated Bit Flags</span></span>

<span data-ttu-id="b87f5-115">Questo attributo non utilizza flag di bit.</span><span class="sxs-lookup"><span data-stu-id="b87f5-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="b87f5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b87f5-116">Remarks</span></span>

<span data-ttu-id="b87f5-117">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="b87f5-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



