---
description: L'inoltro è la deviazione di una sessione in ingresso a un indirizzo di destinazione diverso.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Inoltra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddddd21a945c3ca63a5c9040b8eabe0d1056b74b2f819f3fb62dbd8b760aaca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660851"
---
# <a name="forward"></a>Inoltra

L'inoltro è la deviazione di una sessione in ingresso a un indirizzo di destinazione diverso. TAPI consente a un'applicazione di specificare un elenco di condizioni di inoltro per un indirizzo. Le condizioni di inoltro possono essere con granularità fine come una destinazione e una modalità di inoltro [**diverse**](./lineforwardmode--constants.md) per ogni indirizzo chiamante.

L'operazione di inoltro può essere usata anche per implementare una funzionalità di non disturbo selettiva, inoltrando alcuni chiamanti alla posta vocale e consentendo ad altri di tentare il completamento.

L'operazione di inoltro può anche annullare qualsiasi inoltro attualmente attivo.

Alcuni provider di servizi richiedono che un'applicazione crei una chiamata di consulenza prima di un'operazione di inoltro. All'operazione di inoltro viene quindi passato un puntatore alla chiamata di consulenza.

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Per impostare [**lineForward per**](/windows/win32/api/tapi/nf-tapi-lineforward) ottenere [**lineGetAddressStatus,**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)modificare il messaggio di notifica [**LINE \_ ADDRESSSTATE**](./line-addressstate.md) con LINEADDRESSSTATE \_ FORWARD.

**TAPI 3.x:** Vedere [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), notifica di modifica: [**ITAddressEvent::get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ FORWARD.

> [!Note]  
> Potrebbe essere impossibile per un provider di servizi sapere in qualsiasi momento quale inoltro è in vigore per un indirizzo. L'inoltro può essere annullato o modificato in modi che non comportano la notifica al provider di servizi.

 

 

 
