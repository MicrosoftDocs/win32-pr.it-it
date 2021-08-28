---
description: L'operazione di trasferimento consente a un'applicazione di inviare una sessione di comunicazione attualmente connessa a un indirizzo diverso.
ms.assetid: b1027f09-74e1-4da8-b718-bb55a56dda1d
title: Trasferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bb527ad8e0a26ba5e4da341eb15509e8af05e7950d82de92be839e70370c79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514541"
---
# <a name="transfer"></a>Trasferimento

L'operazione di trasferimento consente a un'applicazione di inviare una sessione di comunicazione attualmente connessa a un indirizzo diverso.

TAPI offre due meccanismi per il trasferimento di una sessione corrente a un indirizzo diverso. *Il trasferimento non* vedente consente il trasferimento di una sessione esistente a un indirizzo di destinazione specificato in un'unica fase. *Il trasferimento* di consulenza richiede l'esistenza di una sessione di consulenza oltre alla sessione corrente da configurare per il trasferimento e quindi il completamento del trasferimento. La scelta tra questi due tipi è spesso basata sulle funzionalità del provider di servizi perché alcuni provider di servizi non supportano il trasferimento blind. In alcuni casi, le esigenze dell'applicazione possono rendere il trasferimento consultivo il metodo preferito anche quando è possibile il trasferimento non vedente.

L'operazione di trasferimento non vedente è fondamentalmente la stessa in TAPI 2 e TAPI 3, ma il trasferimento consultivo segue modelli leggermente diversi.

**TAPI 2.x:** Il trasferimento consultivo inizia con la chiamata [**a lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), che inserisce la chiamata esistente in attesa di consulenza e identifica questa chiamata come destinazione per la richiesta di trasferimento-completamento successiva. La **funzione lineSetupTransfer** alloca anche una chiamata di consulenza che può essere usata per stabilire la chiamata di consultazione con la parte a cui verrà trasferita la chiamata. L'applicazione può comporre l'estensione della parte di destinazione nella chiamata di consulenza (usando [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)) oppure può eliminare e deallocare la chiamata di consulenza e attivare invece una chiamata esistente mantenuta (usando [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold)), se supportata dall'opzione . Mentre la chiamata iniziale è in attesa di consulenza e la chiamata di consulenza è attiva, l'applicazione può alternare tra queste chiamate usando [**lineSwapHold**](/windows/win32/api/tapi/nf-tapi-lineswaphold).

**TAPI 2.x:** Le applicazioni completano il trasferimento consultivo [**usando lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer). Entrambe le chiamate verranno ripristinate allo *stato inattivo.*

Le applicazioni possono usare la funzionalità "trasferimento in un passaggio" di molti PBX (un singolo pulsante che preme per stabilire un trasferimento consulto) impostando il parametro *lpCallParams* sul membro **LINECALLPARAMFLAGS \_ ONESTEPTRANSFER** delle costanti [LINECALLPARAMFLAGS \_](./linecallparamflags--constants.md) quando si chiama [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer).

**TAPI 3.x:** Il trasferimento consultivo inizia con [**l'uso di ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) per creare una chiamata consultiva al nuovo indirizzo di destinazione. [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer) viene quindi chiamato sull'oggetto chiamata originale usando un puntatore al nuovo oggetto chiamata consulto come parametro. La [**chiamata a ITBasicCallControl::Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) sull'oggetto di chiamata consulto completa quindi il trasferimento.

L'applicazione deve rilasciare le risorse di sessione dopo il completamento di un'operazione di trasferimento.

Non tutti i provider di servizi supportano l'uso di questa operazione.

**TAPI 2.x:** Vedere [**lineBlindTransfer**](/windows/win32/api/tapi/nf-tapi-lineblindtransfer), [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer).

**TAPI 3.x:** Vedere [**ITBasicCallControl::BlindTransfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer), [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), [**ITBasicCallControl::Transfer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer), [**ITBasicCallControl::Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish).

 

 
