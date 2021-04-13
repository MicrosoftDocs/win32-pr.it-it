---
title: Registrazione con server dei criteri di rete
description: Registrazione con server dei criteri di rete
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338414"
---
# <a name="logging-with-network-policy-server"></a>Registrazione con server dei criteri di rete

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

Nella tabella seguente vengono descritti solo gli aspetti più importanti dei pacchetti di accounting RADIUS. Il documento sulla richiesta di contabilità RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) fornisce informazioni dettagliate su questi pacchetti.

I pacchetti di accounting RADIUS possono essere divisi nelle categorie seguenti.



| Pacchetto di contabilità  | Descrizione                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Inviato dal server di accesso alla rete (NAS) per indicare che è stato riavviato.<br/> Contiene l'identificatore NAS/IPAddress.<br/>                                                                                        |
| Accounting-Off     | Inviato dal NAS per indicare che è in fase di arresto.<br/> Contiene l'identificatore NAS/IPAddress.<br/>                                                                                                            |
| Accounting-Start   | Inviato dal NAS, dopo che l'utente è stato autenticato e autorizzato, per indicare l'inizio di una sessione utente. <br/> Contiene userid, NAS-Identifier/IPAddress, oltre ad altre informazioni ricevute dal NAS.<br/> |
| Accounting-Stop    | Inviato dal NAS per indicare la fine di una sessione utente.<br/> Contiene userid, NAS-Identifier/IPAddress, oltre ad altre informazioni ricevute dal NAS.<br/>                                                      |
| Accounting-Interim | Potrebbe essere inviato periodicamente dal NAS per ogni utente che ha eseguito l'accesso al server NAS. <br/> Questa funzionalità è in genere supportata nelle versioni più recenti del server NAS.<br/>                                                     |



 

I problemi seguenti sono importanti da considerare quando si raccolgono le informazioni di contabilità rese disponibili tramite RADIUS:

-   In rari casi, è possibile che i pacchetti vengano persi durante la trasmissione e che non raggiungano mai il server RADIUS.
-   Il server RADIUS non riceve alcuna notifica se il NAS viene interrotto.
-   ISDN supporta più sessioni e ogni sessione genera una coppia di pacchetti Accounting-Start/Stop. È presente un attributo contabilità denominato identificatore a più sessioni che identifica chiaramente tali pacchetti multisessione. Verificare l'identificatore di più sessioni oltre all'identificatore di sessione per calcolare il numero di sessioni.

## <a name="requests-logged-by-nps"></a>Richieste registrate da server dei criteri di server

Per impostazione predefinita, NPS non registra i dati. Il server dei criteri di accesso può essere configurato tramite l'interfaccia utente NPS (NPS. msc) per registrare le richieste seguenti.



| Pacchetto registrato          | Descrizione                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Richiesta accounting     | Tutti i pacchetti di contabilità descritti nella tabella precedente.<br/>                                                                    |
| Richiesta di autenticazione | Inviato dal NAS per conto dell'utente che si connette.<br/> Le voci di log contengono solo attributi in ingresso.<br/>                    |
| Accettazione autenticazione  | Inviato da NPS per indicare che la connessione utente deve essere accettata.<br/> Le voci di log contengono solo attributi in uscita.<br/> |
| Rifiuto autenticazione  | Inviato da NPS per indicare che la connessione utente deve essere rifiutata.<br/> Le voci di log contengono solo attributi in uscita.<br/> |



 

I dati registrati da NPS possono accedere a un file di testo nel server NPS o a un database SQL centrale. Per ulteriori informazioni sulla registrazione di NPS SQL, vedere [programmabilità SQL](sql-programmability.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio di autenticazione Internet e server dei criteri di rete](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticazione, autorizzazione e accounting RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Utilizzo di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

