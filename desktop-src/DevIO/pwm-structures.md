---
description: 'Altre informazioni su: strutture PWM'
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: Strutture PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966084"
---
# <a name="pwm-structures"></a><span data-ttu-id="8ff0d-103">Strutture PWM</span><span class="sxs-lookup"><span data-stu-id="8ff0d-103">PWM Structures</span></span>

<span data-ttu-id="8ff0d-104">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="8ff0d-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ff0d-105">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="8ff0d-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ff0d-106">Con la modulazione della larghezza del polso vengono usate le strutture seguenti:</span><span class="sxs-lookup"><span data-stu-id="8ff0d-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8ff0d-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8ff0d-107">In this section</span></span>



| <span data-ttu-id="8ff0d-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="8ff0d-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="8ff0d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ff0d-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ff0d-110">**il \_ controller PWM \_ Ottiene l' \_ \_ output del periodo effettivo \_**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="8ff0d-111">Contiene il periodo di segnale di output effettivo per un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="8ff0d-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="8ff0d-112">**\_informazioni sul controller PWM \_**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="8ff0d-113">Rappresenta le informazioni statiche che caratterizzano un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="8ff0d-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="8ff0d-114">**\_input del \_ \_ periodo desiderato \_ impostato \_ dal controller PWM**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="8ff0d-115">Contiene un valore di input per un periodo di segnale suggerito per il controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="8ff0d-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="8ff0d-116">**\_output del \_ \_ periodo desiderato \_ del set di controller PWM \_**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="8ff0d-117">Contiene il periodo effettivo del segnale di output del controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="8ff0d-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="8ff0d-118">**\_ \_ \_ \_ \_ \_ output percentuale ciclo di dazio attivo Get \_ pin PWM**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="8ff0d-119">Contiene la percentuale del ciclo di lavoro corrente per un PIN o un canale in un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="8ff0d-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="8ff0d-120">**\_input della \_ \_ percentuale del \_ ciclo di lavoro attivo \_ impostato \_ dal pin \_ PWM**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="8ff0d-121">Contiene una percentuale del ciclo di lavoro desiderata per un PIN o un canale in un controller PWM (Pulse Width Modulation).</span><span class="sxs-lookup"><span data-stu-id="8ff0d-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="8ff0d-122">**\_output della \_ \_ polarità del pin PWM \_**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="8ff0d-123">Contiene un valore di polarità da restituire.</span><span class="sxs-lookup"><span data-stu-id="8ff0d-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="8ff0d-124">**\_input di \_ \_ polarità set pin PWM \_**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="8ff0d-125">Contiene un valore desiderato per la polarità di un PIN o di un canale.</span><span class="sxs-lookup"><span data-stu-id="8ff0d-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="8ff0d-126">**l' \_ output del pin PWM \_ è stato \_ avviato \_**</span><span class="sxs-lookup"><span data-stu-id="8ff0d-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="8ff0d-127">Contiene lo stato corrente di generazione del segnale di un PIN.</span><span class="sxs-lookup"><span data-stu-id="8ff0d-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 




