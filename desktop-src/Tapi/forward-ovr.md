---
description: L'invio è la deviazione di una sessione in ingresso a un indirizzo di destinazione diverso.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Inoltra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879262"
---
# <a name="forward"></a>Inoltra

L'invio è la deviazione di una sessione in ingresso a un indirizzo di destinazione diverso. TAPI consente a un'applicazione di specificare un elenco di condizioni di invio per un indirizzo. Le condizioni di inoltri possono essere con granularità fine come una destinazione e una [**modalità di invio**](./lineforwardmode--constants.md) diverse per ogni indirizzo del chiamante.

L'operazione di invio può essere usata anche per implementare una funzionalità selettiva di non disturbo, tramite l'invio di alcuni chiamanti alla posta vocale e consentire ad altri di provare il completamento.

L'operazione di invio può inoltre annullare eventuali inoltri attualmente in vigore.

Alcuni provider di servizi richiedono che un'applicazione crei una chiamata di consultazione prima di un'operazione di invio. All'operazione di invio viene quindi passato un puntatore alla chiamata di consultazione.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Per impostare [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) in modo da ottenere [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), modificare il messaggio di notifica della [**riga \_ ADDRESSSTATE**](./line-addressstate.md) con LINEADDRESSSTATE \_ in futuro.

**TAPI 3. x:** Vedere [**ITAddress:: inoltr**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress:: Get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), Change Notification: [**ITADDRESSEVENT:: Get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) con AE \_ in futuro.

> [!Note]  
> Potrebbe non essere possibile per un provider di servizi conoscere sempre l'avanzamento per un indirizzo. L'invio può essere annullato o modificato in modo che non comporti notifiche al provider di servizi.

 

 

 
