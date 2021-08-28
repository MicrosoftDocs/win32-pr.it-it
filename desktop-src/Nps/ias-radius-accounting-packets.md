---
title: Registrazione con il server dei criteri di rete
description: Registrazione con il server dei criteri di rete
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c6446a6ece75a8da8e51ecab3ed4b6ebf256360e8d9032a676922b83b664d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778071"
---
# <a name="logging-with-network-policy-server"></a>Registrazione con il server dei criteri di rete

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.

 

Nella tabella seguente vengono descritti solo gli aspetti più importanti dei pacchetti di accounting RADIUS. Il documento RADIUS Accounting Request for Comments[(RFC 2866)](https://www.ietf.org/rfc/rfc2866.txt)fornisce informazioni dettagliate su questi pacchetti.

I pacchetti di accounting RADIUS possono essere suddivisi nelle categorie seguenti.



| Pacchetto di accounting  | Descrizione                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Inviato dal server di accesso alla rete (NAS) per indicare che è stato riavviato.<br/> Contiene nas-identifier/ipaddress.<br/>                                                                                        |
| Accounting-Off     | Inviato dal NAS per indicare che è in fase di arresto.<br/> Contiene nas-identifier/ipaddress.<br/>                                                                                                            |
| Accounting-Start   | Inviato dal NAS, dopo che l'utente è stato autenticato e autorizzato, per indicare l'avvio di una sessione utente. <br/> Contiene l'ID utente, l'identificatore nas/ipaddress e altre informazioni ricevute dal NAS.<br/> |
| Accounting-Stop    | Inviato dal NAS per indicare la fine di una sessione utente.<br/> Contiene l'ID utente, l'identificatore nas/ipaddress e altre informazioni ricevute dal NAS.<br/>                                                      |
| Accounting-Interim | Può essere inviato periodicamente dal NAS per ogni utente connesso al NAS. <br/> Questa funzionalità è in genere supportata nelle versioni più recenti di NAS.<br/>                                                     |



 

Quando si raccolgono informazioni di accounting rese disponibili tramite RADIUS, è importante considerare i problemi seguenti:

-   In rari casi, i pacchetti potrebbero andare persi durante la trasmissione e non raggiungere mai il server RADIUS.
-   Il server RADIUS non viene informato se il NAS viene interrotto.
-   ISDN supporta più sessioni e ogni sessione genera una coppia di pacchetti Accounting-Start/Stop. Esiste un attributo di accounting denominato identificatore a più sessioni che identifica chiaramente tali pacchetti a più sessioni. Controllare l'identificatore multi-sessione oltre all'identificatore di sessione per calcolare il numero di sessioni.

## <a name="requests-logged-by-nps"></a>Richieste registrate da Server dei criteri di rete

Per impostazione predefinita, Server dei criteri di rete non registra alcun dato. È possibile configurare Server dei criteri di rete usando l'interfaccia utente di Server dei criteri di rete (nps.msc) per registrare le richieste seguenti.



| Pacchetto registrato          | Descrizione                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Richiesta di accounting     | Uno dei pacchetti di accounting descritti nella tabella precedente.<br/>                                                                    |
| Richiesta di autenticazione | Inviato dal NAS per conto dell'utente che si connette.<br/> Le voci di log contengono solo attributi in ingresso.<br/>                    |
| Accettazione dell'autenticazione  | Inviato da Server dei criteri di rete per indicare che la connessione utente deve essere accettata.<br/> Le voci di log contengono solo attributi in uscita.<br/> |
| Autenticazione rifiutata  | Inviato dal server dei criteri di rete per indicare che la connessione utente deve essere rifiutata.<br/> Le voci di log contengono solo attributi in uscita.<br/> |



 

I dati registrati da Server dei criteri di rete possono passare a un file di testo nel server dei criteri di rete o in un database SQL centrale. Per altre informazioni sulla registrazione SQL server dei criteri di rete, [vedere SQL Programmabilità](sql-programmability.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticazione, autorizzazione e accounting RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Uso di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

