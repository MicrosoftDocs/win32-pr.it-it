---
description: L'operazione di prelievo consente a un'applicazione di rispondere a una sessione che invia avvisi a un altro indirizzo. L'applicazione identifica la destinazione del pickup e restituisce un identificatore di sessione per la chiamata selezionata.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Prelievo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758336"
---
# <a name="pickup"></a>Prelievo

L'operazione di prelievo consente a un'applicazione di rispondere a una sessione che invia avvisi a un altro indirizzo. L'applicazione identifica la destinazione del pickup e restituisce un identificatore di sessione per la chiamata selezionata.

Esistono diversi modi per identificare la destinazione della richiesta di prelievo. In primo luogo, l'applicazione può specificare l'indirizzo della parte di avviso. In secondo luogo, se non viene specificato alcun indirizzo e l'opzione lo consente, l'applicazione può prelevare qualsiasi sessione di avviso nel gruppo di prelievo. In terzo luogo, alcuni commutatori consentono il ritiro di un avviso di sessione in un gruppo di prelievo diverso se viene specificato l'identificatore di gruppo.

Alcuni sistemi telefonici principali supportano un *trasferimento tramite* la funzionalità di attesa su un aspetto di chiamata Bridged-Exclusive. In questo schema, un telefono specifico è proprietario di una chiamata esclusivamente quando la chiamata è attiva, ma quando la chiamata è in attesa, qualsiasi telefono con un aspetto della linea può prelevare la chiamata.

**TAPI 2. x:** Un'applicazione può usare un'operazione di prelievo con un indirizzo di destinazione **null** a questo scopo, in modo analogo a come viene usata la funzione per prelevare una chiamata in attesa su una linea analoga. LINEADDRFEATURE \_ PICKUPHELD indica l'esistenza della funzionalità.

Se LINEADDRCAPFLAGS \_ PICKUPCALLWAIT è **true**, è possibile prelevare una sessione per la quale l'utente ha rilevato in modo udibile il segnale in attesa di chiamata, ma per il quale il provider di servizi non è in grado di eseguire il rilevamento. Questo consente all'utente un meccanismo per "rispondere" a una chiamata in attesa anche se il provider di servizi non è stato in grado di rilevare il segnale in attesa di chiamata. Sia l'indirizzo di destinazione che l'ID gruppo devono essere **null** per scegliere una chiamata in attesa.

Quando una sessione viene prelevata correttamente, l'applicazione riceve una notifica di modifica dello stato con il [motivo](reason-ovr.md) impostato su LINECALLREASON \_ pickup.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).

**TAPI 3. x:** Vedere [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).

 

 
