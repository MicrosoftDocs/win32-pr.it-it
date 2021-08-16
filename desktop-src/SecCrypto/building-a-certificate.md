---
description: Vengono illustrate le chiamate necessarie per compilare un certificato.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Compilazione di un certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e497f20e8a20d4e401ce89a85d1f8a312dad76865a6c3dfb523d8f2526125c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772976"
---
# <a name="building-a-certificate"></a>Compilazione di un certificato

L'ordine delle chiamate nella compilazione di un certificato è il seguente:

1.  [*L'autorità*](../secgloss/c-gly.md) di certificazione (CA) inizializza i moduli tramite chiamate a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (si verifica una volta durante l'inizializzazione del server). La CA inizializza i criteri e chiude i moduli chiamando [**ICertPolicy2::Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) e [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  L'intermediario chiama la CA tramite [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (si verifica una volta per ogni inizializzazione intermedia). L'intermediario trova la stringa di configurazione necessaria chiamando [**ICertConfig::GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  Il client chiama l'intermediario tramite un'interfaccia specifica dell'intermediario (si verifica una volta per ogni richiesta). Il client invia una [*richiesta di certificato*](../secgloss/c-gly.md) all'intermediario. Può trattarsi, ad esempio, di microsoft Internet Explorer l'invio di una richiesta tramite [il controllo di registrazione certificati](certificate-enrollment-control.md) Microsoft Internet Information Services.
4.  Da intermediario a CA tramite [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (si verifica una volta per ogni richiesta). L'intermediario invia la richiesta di certificato alla CA [**tramite ICertRequest::Submit.**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) Nel caso di Internet Information Services, questa operazione può essere eseguita tramite script Active Server Pages.
5.  L'autorità di certificazione chiama il modulo criteri tramite [**l'interfaccia ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (si verifica una volta per ogni richiesta). L'autorità di certificazione notifica al modulo criteri che una richiesta è stata inviata chiamando [**ICertPolicy::VerifyRequest.**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) Il modulo criteri può esaminare la richiesta e modificare il certificato chiamando i metodi [**dell'interfaccia ICertServerPolicy.**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) Il modulo criteri può quindi indicare che la richiesta è OK (in questo caso, il certificato viene compilato a questo punto), che la richiesta deve essere negata o che la richiesta deve essere sospesa.
6.  (Facoltativo) L'amministratore chiama la CA tramite [**l'interfaccia ICertAdmin.**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) Se la richiesta viene sospesa, l'amministratore può inviare di nuovo o rifiutare la richiesta o modificare gli attributi e le estensioni della richiesta. Si noti che se la richiesta viene inviata di nuovo, il modulo criteri avrà un'altra opportunità di elaborare la richiesta (in seguito a una chiamata a [**ICertPolicy::VerifyRequest).**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) L'attività di nuovo invio o rifiuto della richiesta può essere eseguita tramite lo snap-in MMC Autorità di certificazione o un'altra applicazione che **usa ICertAdmin**.
7.  La CA chiama il modulo exit tramite [**l'interfaccia ICertExit.**](/windows/desktop/api/Certexit/nn-certexit-icertexit) Se il modulo di uscita ha indicato (quando È stato chiamato [**ICertExit::Initialize,**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) nel passaggio 1) che è interessato a visualizzare i certificati rilasciati o le richieste mantenute in sospeso, la CA chiamerà [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  Il modulo exit chiama la CA tramite [**l'interfaccia ICertServerExit.**](/windows/desktop/api/Certif/nn-certif-icertserverexit) Il modulo di uscita può esaminare la richiesta e il nuovo certificato chiamando i metodi di **ICertServerExit.**

 

 
