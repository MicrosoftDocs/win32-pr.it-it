---
description: Questo argomento elenca le IOCTL per la modulazione della larghezza del polso.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: Codici di controllo PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7de81b26a1970bbecde76729be2f1c84e6c067
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965944"
---
# <a name="pwm-control-codes"></a>Codici di controllo PWM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questo argomento elenca le IOCTL per la modulazione della larghezza del polso.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_controller IOCTL PWM \_ ottiene il \_ \_ \_ periodo effettivo**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Recupera il periodo effettivo del segnale di output del controller PWM (Pulse Width Modulation), perché verrebbe misurato nei canali di output.<br/>                                                                                                                                                                                  |
| [**\_informazioni sul \_ controller IOCTL PWM \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Recupera informazioni su un controller PWM (Pulse Width Modulation). Queste informazioni non cambiano dopo l'inizializzazione del controller. <br/>                                                                                                                                                                                |
| [**\_ \_ \_ periodo desiderato del set di controller \_ IOCTL \_ IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Imposta il periodo del segnale di output di un controller PWM (Pulse Width Modulation) su un valore suggerito. <br/>                                                                                                                                                                                                                            |
| [**\_percentuale del \_ ciclo di lavoro per pin PWM \_ get \_ attivo \_ \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Recupera la percentuale del ciclo di lavoro corrente per un PIN o un canale. Il codice di controllo restituisce la percentuale come un [**pin PWM ottenere la struttura di \_ \_ \_ \_ \_ \_ \_ output del ciclo di lavoro attivo**](pwm-pin-get-active-duty-cycle-percentage-output.md) .<br/>                                                                                  |
| [**\_percentuale del \_ \_ ciclo di \_ \_ dazio attivo \_ set \_ di pin IOCTL**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Impostare un valore percentuale del ciclo di lavoro desiderato per il PIN o il canale del controller. Il codice di controllo specifica la percentuale come un [**pin PWM imposta la struttura di \_ \_ \_ \_ \_ \_ \_ input percentuale del ciclo di lavoro attivo**](pwm-pin-set-active-duty-cycle-percentage-input.md) . <br/>                                                                      |
| [**\_ \_ \_ polarità pin IOCTL \_ PWM**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Recupera la polarità del segnale corrente del PIN o del canale. Il codice di controllo ottiene la polarità del segnale come un [**pin PWM ottenere la struttura di \_ \_ \_ \_ output della polarità**](pwm-pin-get-polarity-output.md) . La polarità del segnale è alta o attiva bassa, come definito nell'enumerazione di [**\_ polarità PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) . <br/> |
| [**\_ \_ \_ polarità del set di pin PWM IOCTL \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Imposta la polarità del segnale del PIN o del canale. Il codice di controllo imposta la polarità del segnale in base a una struttura di [**\_ \_ \_ \_ input di polarità del set di pin PWM**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) . La polarità del segnale è alta o attiva bassa, come definito nell'enumerazione di [**\_ polarità PWM**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) .<br/>           |
| [**\_ \_ avvio pin di IOCTL PWM \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Avvia la generazione del segnale PWM (Pulse Width Modulation) su un PIN o un canale. Per verificare se un PIN è stato avviato, [**usare \_ IOCTL \_ PWM \_ pin \_ avviato**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**\_ \_ arresto pin di IOCTL PWM \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Arresta la generazione del segnale PWM (Pulse Width Modulation) su un PIN o un canale. Per verificare se un PIN è stato avviato, [**usare \_ IOCTL \_ PWM \_ pin \_ avviato**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**\_pin PWM di IOCTL \_ \_ \_ avviato**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Recupera lo stato della generazione del segnale per un PIN o un canale. Ogni pin è stato avviato o arrestato perché [**\_ è stata \_ \_ avviata \_**](pwm-pin-is-started-output.md) la struttura di output di un pin PWM.<br/>                                                                                                                                 |



 

 

 




