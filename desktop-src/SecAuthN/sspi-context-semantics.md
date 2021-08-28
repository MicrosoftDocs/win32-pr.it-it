---
description: Un contesto di sicurezza è il set di attributi di sicurezza e regole in vigore durante una sessione di comunicazione.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semantica del contesto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423ce097d1ab71cf50983285f3ca8731497ed5a9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482537"
---
# <a name="sspi-context-semantics"></a>Semantica del contesto SSPI

Un [*contesto di sicurezza*](../secgloss/s-gly.md) è il set di attributi di sicurezza e regole in vigore durante una sessione di comunicazione. Sono incluse informazioni quali le identità dell'entità e le informazioni sulle chiavi, le crittografie e gli algoritmi usati. Per [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), un contesto di sicurezza è una struttura opaca creata tramite uno scambio che coinvolge la funzione [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e la funzione [**AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Per altre informazioni sugli attributi di contesto, vedere [Requisiti di contesto](context-requirements.md).

Il modello SSPI supporta tre tipi di contesti di sicurezza.




| Tipo | Descrizione | 
|------|-------------|
| <a href="connection-oriented-contexts.md">Connection</a> | Un contesto <a href="/windows/desktop/SecGloss/c-gly"><em>orientato alla</em></a> connessione è il contesto di sicurezza più comune e il più semplice da usare. Il chiamante è responsabile del formato complessivo del messaggio e della posizione dei dati nel messaggio. Il chiamante è anche responsabile della posizione dei campi rilevanti per la sicurezza all'interno di un messaggio, ad esempio la posizione dei dati della firma.<br /> | 
| <a href="datagram-contexts.md">Datagram</a> | Un <a href="/windows/desktop/SecGloss/d-gly"><em>contesto orientato</em></a>al datagramma include un supporto aggiuntivo per la comunicazione di datagrammi in stile DCE. Può anche essere usato in modo generico per un'applicazione di trasporto orientata ai datagrammi.<br /><blockquote><p>[!Important]</p><p>Il <a href="microsoft-kerberos.md">pacchetto Kerberos Microsoft</a> non supporta contesti di datagrammi in modalità da utente a utente.<br /></p></blockquote><br /> | 
| <a href="stream-contexts.md">Stream</a> | Un contesto orientato al flusso è responsabile della formattazione del blocco e dei messaggi all'interno del pacchetto di sicurezza. Il chiamante non è interessato alla formattazione, ma piuttosto a un flusso non elaborato di dati.<br /> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti di contesto](context-requirements.md)
</dt> <dt>

[Contesti orientati alla connessione](connection-oriented-contexts.md)
</dt> <dt>

[Contesti di datagrammi](datagram-contexts.md)
</dt> <dt>

[Contesti di flusso](stream-contexts.md)
</dt> </dl>

 

 
