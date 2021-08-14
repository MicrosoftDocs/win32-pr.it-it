---
description: Questo argomento elenca gli IOCTL per pulse width modulation.
ms.assetid: 2ED7A06A-A7EC-4C44-AB22-4A52CF2DF2C5
title: Codici di controllo PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d9118d51721165860d6132cb7f0fc91a0ac95e7a9d92446df27076a625c83b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405205"
---
# <a name="pwm-control-codes"></a>Codici di controllo PWM

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questo argomento elenca gli IOCTL per pulse width modulation.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OTTENERE IL PERIODO EFFETTIVO DEL \_ CONTROLLER IOCTL PWM \_ \_ \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_actual_period)<br/>                   | Recupera il periodo di segnale di output effettivo del controller Pulse Width Modulation (PWM) come verrebbe misurato sui canali di output.<br/>                                                                                                                                                                                  |
| [**INFORMAZIONI SUL CONTROLLER \_ IOCTL PWM \_ \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_get_info)<br/>                                      | Recupera informazioni su un controller PWM (Pulse Width Modulation). Queste informazioni non cambiano dopo l'inizializzazione del controller. <br/>                                                                                                                                                                                |
| [**IOCTL \_ PWM \_ CONTROLLER \_ SET \_ DESIRED \_ PERIOD**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_controller_set_desired_period)<br/>                 | Imposta il periodo di segnale di output di un controller PWM (Pulse Width Modulation) su un valore suggerito. <br/>                                                                                                                                                                                                                            |
| [**PERCENTUALE CICLO DI \_ LAVORO ATTIVO DEL PIN PWM IOCTL \_ \_ \_ \_ \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_active_duty_cycle_percentage)<br/> | Recupera la percentuale del ciclo di lavoro corrente per un pin o un canale. Il codice di controllo restituisce la percentuale come struttura [**PWM \_ PIN GET ACTIVE DUTY CYCLE PERCENTAGE \_ \_ \_ \_ \_ \_ OUTPUT.**](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/>                                                                                  |
| [**IOCTL PWM PIN SET ACTIVE DUTY CYCLE PERCENTAGE (PERCENTUALE CICLO DI LAVORO ATTIVO IMPOSTATO \_ \_ SU PWM \_ \_ \_ \_ \_ IOCTL)**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_active_duty_cycle_percentage)<br/> | Impostare un valore percentuale del ciclo di lavoro desiderato per il pin o il canale del controller. Il codice di controllo specifica la percentuale come struttura [**PWM \_ PIN SET ACTIVE DUTY CYCLE PERCENTAGE \_ \_ \_ \_ \_ \_ INPUT.**](pwm-pin-set-active-duty-cycle-percentage-input.md) <br/>                                                                      |
| [**IOCTL \_ PWM \_ PIN \_ GET \_ POLARITY**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_get_polarity)<br/>                                            | Recupera la polarità del segnale corrente del pin o del canale. Il codice di controllo ottiene la polarità del segnale come [**struttura \_ PWM PIN GET \_ \_ POLARITY \_ OUTPUT.**](pwm-pin-get-polarity-output.md) La polarità del segnale è Active High o Active Low, come definito [**nell'enumerazione PWM \_ POLARITY.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) <br/> |
| [**POLARITÀ DEL \_ SET DI PIN IOCTL PWM \_ \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_set_polarity)<br/>                                            | Imposta la polarità del segnale del pin o del canale. Il codice di controllo imposta la polarità del segnale in base a una [**struttura PWM \_ PIN SET \_ \_ POLARITY \_ INPUT.**](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input) La polarità del segnale è Active High o Active Low, come definito [**nell'enumerazione PWM \_ POLARITY.**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity)<br/>           |
| [**AVVIO \_ PIN PWM IOCTL \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_start)<br/>                                                           | Avvia la generazione del segnale Pulse Width Modulation (PWM) su un pin o un canale. Per verificare se un pin è stato avviato, usare [**IL \_ PIN PWM IOCTL \_ IS \_ \_ STARTED**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                |
| [**ARRESTO \_ PIN PWM IOCTL \_ \_**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_stop)<br/>                                                             | Arresta la generazione del segnale PWM (Pulse Width Modulation) su un pin o un canale. Per verificare se un pin è stato avviato, usare [**IL \_ PIN PWM IOCTL \_ IS \_ \_ STARTED**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**).<br/>                                                                                                                                 |
| [**IL PIN PWM IOCTL \_ \_ È STATO \_ \_ AVVIATO**](/windows/desktop/api/Pwm/ni-pwm-ioctl_pwm_pin_is_started)<br/>                                                | Recupera lo stato di generazione del segnale per un pin o un canale. Ogni pin ha lo stato avviato o arrestato come struttura [**DI OUTPUT IS STARTED \_ \_ \_ DEL \_ PIN PWM.**](pwm-pin-is-started-output.md)<br/>                                                                                                                                 |



 

 

 




