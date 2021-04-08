---
description: L'operazione di trasferimento consente a un'applicazione di inviare una sessione di comunicazione attualmente connessa a un indirizzo diverso.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Trasferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724b9ade43e41ab95a5baa6dfe7d3269f4e4a174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050063"
---
# <a name="transfer"></a>Trasferimento

L'operazione di trasferimento consente a un'applicazione di inviare una sessione di comunicazione attualmente connessa a un indirizzo diverso.

TAPI fornisce due meccanismi per trasferire una sessione corrente a un indirizzo diverso. Il trasferimento in modo *cieco* consente di trasferire una sessione esistente a un indirizzo di destinazione specificato in una fase. Il *trasferimento di consultazioni* richiede l'esistenza di una sessione di consultazione oltre alla sessione corrente per la configurazione per il trasferimento e quindi il completamento del trasferimento. La scelta tra questi due tipi è spesso basata sulle funzionalità del provider di servizi perché alcuni provider di servizi non supportano il trasferimento in modalità cieca. In alcuni casi, le esigenze dell'applicazione possono far trasferire il consultivo al metodo preferito anche laddove è possibile il trasferimento cieco.

L'operazione di trasferimento cieco è fondamentalmente la stessa in TAPI 2 e TAPI 3, ma il trasferimento consultivo segue modelli leggermente diversi.

**TAPI 2. x:** Il trasferimento consultivo inizia con la chiamata a [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), che inserisce la chiamata esistente sulla condizione di consultazione e identifica la chiamata come destinazione per la richiesta di completamento del trasferimento successiva. La funzione **lineSetupTransfer** alloca inoltre una chiamata di consultazione che può essere utilizzata per stabilire la chiamata di consultazione con l'entità alla quale verrà trasferita la chiamata. L'applicazione può comporre l'estensione dell'entità di destinazione nella chiamata di consultazione (usando [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)) oppure può eliminare e deallocare la chiamata di consultazione e attivare invece una chiamata a esistente (usando [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), se supportata dall'opzione. Mentre la chiamata iniziale è in attesa di consultazione e la chiamata di consultazione è attiva, l'applicazione può alternare queste chiamate usando [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2. x:** Le applicazioni completano il trasferimento consultivo usando [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer). Entrambe le chiamate verranno ripristinate allo stato *inattivo* .

Le applicazioni possono usare la funzionalità di trasferimento in un solo passaggio di molti PBX (un singolo pulsante premere per stabilire un trasferimento di consultazione) impostando il parametro *lpCallParams* sul membro **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** delle [ \_ costanti LINECALLPARAMFLAGS](./linecallparamflags--constants.md) quando si chiama [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3. x:** Il trasferimento consultivo inizia con l'uso di [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) per creare una chiamata di consultazione al nuovo indirizzo di destinazione. [**ITBasicCallControl:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) viene quindi chiamato sull'oggetto chiamata originale utilizzando un puntatore al nuovo oggetto chiamata di consultazione come parametro. Se si chiama [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) nell'oggetto chiamata di consultazione, il trasferimento viene completato.

L'applicazione deve rilasciare le risorse della sessione in seguito al completamento di un'operazione di trasferimento.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3. x:** Vedere [**ITBasicCallControl:: BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl:: Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl:: Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
