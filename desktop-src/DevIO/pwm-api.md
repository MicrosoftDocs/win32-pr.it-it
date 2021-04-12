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
# <a name="pwm-api"></a>API PWM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Pulse Width Modulation (PWM) è la tecnica della generazione di un'onda a impulsi rettangolari con una larghezza a impulsi modulata in modo da determinare la variazione del valore medio della forma d'onda. Gli utilizzi più comuni includono la Guida di motori di servo, la luminosità dei LED o altre funzioni correlate. PWM è progettato per essere usato principalmente per gli scenari di Internet delle cose.

## <a name="about-pulse-width-modulation"></a>Informazioni sulla modulazione della larghezza del polso

Una forma d'onda PWM può essere categorizzata in base a due parametri:

-   Un periodo di forma d'onda (T)

-   Il ciclo di lavoro, in cui la frequenza della forma d'onda (f) è il reciproco del periodo f = 1/T

Il ciclo di lavoro descrive la proporzione **del** / tempo **attivo** rispetto all'intervallo o al **periodo** di tempo normale. Un ciclo di dazio basso corrisponde a una media di bassa potenza di output, perché la potenza è disattivata per la maggior parte del tempo. Il ciclo di servizio è espresso come percentuale. Il totale su è pari al 100%. Completamente disattivato è 0%. La metà **attiva** del tempo è pari al 50%.

Gli sviluppatori che desiderano implementare PWM nelle applicazioni Internet devono esaminare la [documentazione di WINRT PWM.](/uwp/api/windows.devices.pwm)

## <a name="pulse-width-modulation-types"></a>Tipi di modulazione della larghezza del polso

PWM USA [questi codici di controllo di i](pwm-control-codes.md)/o, [strutture](pwm-structures.md)ed [enumerazioni.](pwm-enumeration-types.md)

PWM usa anche la funzione seguente: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).

 

 
