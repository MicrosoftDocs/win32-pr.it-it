---
description: Un contesto di sicurezza è il set di attributi e regole di sicurezza in vigore durante una sessione di comunicazione.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semantica del contesto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddadd2c8a76f1fdc151273dca2027b8cb55776a50b78a7c08343c22410ae90e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916980"
---
# <a name="sspi-context-semantics"></a>Semantica del contesto SSPI

Un [*contesto di sicurezza*](../secgloss/s-gly.md) è il set di attributi e regole di sicurezza in vigore durante una sessione di comunicazione. Sono incluse informazioni quali le identità dell'entità e le informazioni sulle chiavi, le crittografie e gli algoritmi in uso. Per [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), un contesto di sicurezza è una struttura opaca creata tramite uno scambio che interessa la funzione [**InitializeSecurityContext (Generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e la funzione [**AcceptSecurityContext (Generale).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)

Per altre informazioni sugli attributi di contesto, vedere [Requisiti di contesto.](context-requirements.md)

Il modello SSPI supporta tre tipi di contesti di sicurezza.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">Connection</a></td>
<td>Un contesto <a href="/windows/desktop/SecGloss/c-gly"><em>orientato alla connessione</em></a> è il contesto di sicurezza più comune e il più semplice da usare. Il chiamante è responsabile del formato complessivo del messaggio e della posizione dei dati nel messaggio. Il chiamante è anche responsabile della posizione dei campi rilevanti per la sicurezza all'interno di un messaggio, ad esempio la posizione dei dati della firma.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagram</a></td>
<td>Un <a href="/windows/desktop/SecGloss/d-gly"><em>contesto orientato</em></a>ai datagrammi include un supporto aggiuntivo per la comunicazione del datagramma di tipo DCE. Può anche essere utilizzato in modo generico per un'applicazione di trasporto orientata ai datagrammi.<br/>
<blockquote>
<p>[!Important]</p>
<p>Il <a href="microsoft-kerberos.md">pacchetto Microsoft Kerberos</a> non supporta contesti di datagramma in modalità utente-utente.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Un contesto orientato al flusso è responsabile della formattazione del blocco e dei messaggi all'interno del pacchetto di sicurezza. Il chiamante non è interessato alla formattazione, ma piuttosto a un flusso di dati non elaborato.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti di contesto](context-requirements.md)
</dt> <dt>

[Contesti orientati alla connessione](connection-oriented-contexts.md)
</dt> <dt>

[Contesti di datagramma](datagram-contexts.md)
</dt> <dt>

[Contesti di flusso](stream-contexts.md)
</dt> </dl>

 

 
