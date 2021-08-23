---
description: L'operazione di ritiro consente a un'applicazione di rispondere a una sessione che invia avvisi a un altro indirizzo. L'applicazione identifica la destinazione del ritiro e viene restituito un identificatore di sessione per la chiamata prelevata.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Pickup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 288510d2d9e2eb2ed6e9a5cc5c58f6957b933b7d43db951eb330dd081a4c446f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873061"
---
# <a name="pickup"></a>Pickup

L'operazione di ritiro consente a un'applicazione di rispondere a una sessione che invia avvisi a un altro indirizzo. L'applicazione identifica la destinazione del ritiro e viene restituito un identificatore di sessione per la chiamata prelevata.

Esistono diversi modi per identificare la destinazione della richiesta di ritiro. In primo luogo, l'applicazione può specificare l'indirizzo della parte che invia avvisi. In secondo luogo, se non viene specificato alcun indirizzo e l'opzione lo consente, l'applicazione può prelevare qualsiasi sessione di avviso nel gruppo di ritiro. In terzo luogo, alcuni commutatori consentono il ritiro di un avviso di sessione in un gruppo di ritiro diverso se viene specificato l'identificatore del gruppo.

Alcuni sistemi telefonici principali supportano *il trasferimento tramite la funzionalità* di blocco nelle chiamate con bridge esclusivo. In questo schema, un particolare telefono è proprietario di una chiamata esclusivamente quando la chiamata è attiva, ma quando la chiamata è in attesa, qualsiasi telefono che ha un aspetto della linea può prelevare la chiamata.

**TAPI 2.x:** Un'applicazione può usare un'operazione di ritiro con un indirizzo di destinazione **NULL** a questo scopo, analogamente a come la funzione viene usata per prelevare una chiamata in attesa di chiamata su una linea analoga. LINEADDRFEATURE \_ PICKUPHELD indica l'esistenza della funzionalità.

Se LINEADDRCAPFLAGS \_ PICKUPCALLWAIT è **TRUE,** è possibile selezionare una sessione per la quale l'utente ha rilevato in modo udibile il segnale di attesa delle chiamate, ma per la quale il provider di servizi non è in grado di eseguire il rilevamento. In questo modo l'utente può "rispondere" a una chiamata in attesa anche se il provider di servizi non è riuscito a rilevare il segnale di attesa delle chiamate. Sia l'indirizzo di destinazione che l'ID del gruppo devono essere **NULL** per prelevare una chiamata in attesa.

Quando una sessione viene prelevata correttamente, l'applicazione riceve una notifica di modifica dello stato con il motivo [impostato](reason-ovr.md) su LINECALLREASON \_ PICKUP.

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Vedere [**linePickup.**](/windows/win32/api/tapi/nf-tapi-linepickup)

**TAPI 3.x:** Vedere [**ITBasicCallControl::P ickup.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup)

 

 
