---
description: Illustra le chiamate necessarie per compilare un certificato.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Compilazione di un certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885442"
---
# <a name="building-a-certificate"></a>Compilazione di un certificato

L'ordine delle chiamate nella compilazione di un certificato è il seguente:

1.  L' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) Inizializza i moduli tramite le chiamate a [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) e [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (si verifica una sola volta durante l'inizializzazione del server). La CA Inizializza i criteri e i moduli di uscita chiamando [**ICertPolicy2:: Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) e [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  L'intermediario chiama la CA tramite [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) (si verifica una volta per inizializzazione intermedia). L'intermediario trova la stringa di configurazione necessaria chiamando [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  Il client chiama l'intermediario attraverso un'interfaccia specifica per l'intermediario (si verifica una volta per ogni richiesta). Il client invia una [*richiesta di certificato*](../secgloss/c-gly.md) all'intermediario. Questo può essere, ad esempio, Microsoft Internet Explorer che invia una richiesta tramite il [controllo di registrazione certificati](certificate-enrollment-control.md) a Microsoft Internet Information Services.
4.  Intermediario per CA tramite [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (si verifica una volta per ogni richiesta). L'intermediario Invia la richiesta di certificato alla CA tramite [**ICertRequest:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit). Nel caso di Internet Information Services, è possibile eseguire questa operazione tramite Active Server script di pagine.
5.  La CA chiama il modulo criteri tramite l'interfaccia [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) (si verifica una volta per ogni richiesta). La CA notifica al modulo criteri che è arrivata una richiesta chiamando [**ICertPolicy:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest). Il modulo criteri può esaminare la richiesta e modificare il certificato chiamando i metodi dell'interfaccia [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Il modulo criteri può quindi indicare che la richiesta è OK (in tal caso, il certificato è compilato a questo punto), la richiesta deve essere negata o la richiesta deve essere sospesa.
6.  Opzionale L'amministratore chiama la CA tramite l'interfaccia [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) . Se la richiesta viene sospesa, l'amministratore può inviare nuovamente o rifiutare la richiesta oppure modificare gli attributi e le estensioni della richiesta. Si noti che se la richiesta viene inviata nuovamente, il modulo criteri avrà un'altra opportunità per elaborare la richiesta (in seguito a una chiamata a [**ICertPolicy:: VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). L'attività di invio o negazione della richiesta può essere eseguita tramite lo snap-in MMC dell'autorità di certificazione o un'altra applicazione che utilizza **ICertAdmin**.
7.  La CA chiama il modulo Exit tramite l'interfaccia [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) . Se il modulo di uscita ha indicato (quando è stato chiamato [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) , nel passaggio 1) che è interessato a visualizzare i certificati rilasciati o le richieste mantenute in sospeso, la CA chiamerà [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify).
8.  Il modulo exit chiama la CA tramite l'interfaccia [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) . Il modulo Exit può esaminare la richiesta e il nuovo certificato chiamando i metodi di **ICertServerExit**.

 

 
