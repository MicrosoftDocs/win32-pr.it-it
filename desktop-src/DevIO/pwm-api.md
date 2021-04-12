---
description: Pulse Width Modulation (PWM) è la tecnica della generazione di un'onda a impulsi rettangolari con una larghezza a impulsi modulata in modo da determinare la variazione del valore medio della forma d'onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523642"
---
# <a name="pwm-api"></a><span data-ttu-id="c5f39-103">API PWM</span><span class="sxs-lookup"><span data-stu-id="c5f39-103">PWM API</span></span>

<span data-ttu-id="c5f39-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="c5f39-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c5f39-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="c5f39-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c5f39-106">Pulse Width Modulation (PWM) è la tecnica della generazione di un'onda a impulsi rettangolari con una larghezza a impulsi modulata in modo da determinare la variazione del valore medio della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="c5f39-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="c5f39-107">Gli utilizzi più comuni includono la Guida di motori di servo, la luminosità dei LED o altre funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="c5f39-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="c5f39-108">PWM è progettato per essere usato principalmente per gli scenari di Internet delle cose.</span><span class="sxs-lookup"><span data-stu-id="c5f39-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="c5f39-109">Informazioni sulla modulazione della larghezza del polso</span><span class="sxs-lookup"><span data-stu-id="c5f39-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="c5f39-110">Una forma d'onda PWM può essere categorizzata in base a due parametri:</span><span class="sxs-lookup"><span data-stu-id="c5f39-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="c5f39-111">Un periodo di forma d'onda (T)</span><span class="sxs-lookup"><span data-stu-id="c5f39-111">A waveform period (T)</span></span>

-   <span data-ttu-id="c5f39-112">Il ciclo di lavoro, in cui la frequenza della forma d'onda (f) è il reciproco del periodo f = 1/T</span><span class="sxs-lookup"><span data-stu-id="c5f39-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="c5f39-113">Il ciclo di lavoro descrive la proporzione **del** / tempo **attivo** rispetto all'intervallo o al **periodo** di tempo normale.</span><span class="sxs-lookup"><span data-stu-id="c5f39-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="c5f39-114">Un ciclo di dazio basso corrisponde a una media di bassa potenza di output, perché la potenza è disattivata per la maggior parte del tempo.</span><span class="sxs-lookup"><span data-stu-id="c5f39-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="c5f39-115">Il ciclo di servizio è espresso come percentuale.</span><span class="sxs-lookup"><span data-stu-id="c5f39-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="c5f39-116">Il totale su è pari al 100%.</span><span class="sxs-lookup"><span data-stu-id="c5f39-116">Fully on is 100%.</span></span> <span data-ttu-id="c5f39-117">Completamente disattivato è 0%.</span><span class="sxs-lookup"><span data-stu-id="c5f39-117">Fully off is 0%.</span></span> <span data-ttu-id="c5f39-118">La metà **attiva** del tempo è pari al 50%.</span><span class="sxs-lookup"><span data-stu-id="c5f39-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="c5f39-119">Gli sviluppatori che desiderano implementare PWM nelle applicazioni Internet devono esaminare la [documentazione di WINRT PWM.](/uwp/api/windows.devices.pwm)</span><span class="sxs-lookup"><span data-stu-id="c5f39-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="c5f39-120">Tipi di modulazione della larghezza del polso</span><span class="sxs-lookup"><span data-stu-id="c5f39-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="c5f39-121">PWM USA [questi codici di controllo di i](pwm-control-codes.md)/o, [strutture](pwm-structures.md)ed [enumerazioni.](pwm-enumeration-types.md)</span><span class="sxs-lookup"><span data-stu-id="c5f39-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="c5f39-122">PWM usa anche la funzione seguente: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span><span class="sxs-lookup"><span data-stu-id="c5f39-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 
