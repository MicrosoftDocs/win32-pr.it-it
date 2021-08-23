---
description: Pulse Width Modulation (PWM) è la tecnica di generazione di un'onda di pulsazione rettangolare con una larghezza di pulsazione che viene modulata per generare la variazione del valore medio della forma d'onda.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: PWM API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff257007180cf3da2b78c14415c8fa350b4bb395e0202f49d2d7ae056f025bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405195"
---
# <a name="pwm-api"></a>PWM API

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Pulse Width Modulation (PWM) è la tecnica di generazione di un'onda di pulsazione rettangolare con una larghezza di pulsazione che viene modulata per generare la variazione del valore medio della forma d'onda. Gli usi più comuni includono la guida di motori servo, LED di attenuazione o altre funzioni correlate. PWM è progettato per essere usato principalmente per Internet delle cose scenari.

## <a name="about-pulse-width-modulation"></a>Informazioni sulla modulazione della larghezza degli pulse

Una forma d'onda PWM può essere categorizzata in base a due parametri:

-   Un periodo di forma d'onda (T)

-   Ciclo di lavoro, in cui la frequenza della forma d'onda (f) è il reciproco del periodo f=1/T

Il ciclo di lavoro descrive la proporzione del **tempo** attivo /  rispetto all'intervallo regolare o **al periodo** di tempo. Un ciclo di lavoro basso corrisponde a una media di potenza di output bassa, perché l'alimentazione è disattivata per la maggior parte del tempo. Il ciclo di lavoro è espresso come percentuale. Completamente on è 100%. Completamente disattivato è 0%. **La metà** del tempo attiva è del 50%.

Gli sviluppatori che desiderano implementare PWM nelle applicazioni IoT devono esaminare la [documentazione di WinRT PWM.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Tipi di modulazione pulse width

PWM usa [questi codici di controllo I/O,](pwm-control-codes.md) [strutture](pwm-structures.md)ed [enumerazioni.](pwm-enumeration-types.md)

PWM usa anche la funzione seguente: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
