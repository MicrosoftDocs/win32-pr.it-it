---
description: Un contesto di sicurezza è il set di attributi di sicurezza e regole attive durante una sessione di comunicazione.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Semantica del contesto SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316215"
---
# <a name="sspi-context-semantics"></a>Semantica del contesto SSPI

Un [*contesto di sicurezza*](../secgloss/s-gly.md) è il set di attributi di sicurezza e regole attive durante una sessione di comunicazione. Sono incluse informazioni quali le identità del principale e le informazioni sulle chiavi, le crittografie e gli algoritmi utilizzati. Per [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI), un contesto di sicurezza è una struttura opaca creata tramite uno scambio che interessa la funzione [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) e la funzione [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Per ulteriori informazioni sugli attributi di contesto, vedere [requisiti di contesto](context-requirements.md).

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
<td>Un <a href="/windows/desktop/SecGloss/c-gly"><em>contesto</em></a> orientato alla connessione è il contesto di sicurezza più comune e più semplice da usare. Il chiamante è responsabile del formato generale del messaggio e della posizione dei dati nel messaggio. Il chiamante è inoltre responsabile della posizione dei campi relativi alla sicurezza all'interno di un messaggio, ad esempio la posizione dei dati della firma.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagram</a></td>
<td>Un contesto orientato ai <a href="/windows/desktop/SecGloss/d-gly"><em>datagramma</em></a>ha un supporto aggiuntivo per la comunicazione del datagramma di tipo DCE. Può anche essere usato in modo generico per un'applicazione di trasporto orientata ai datagramma.<br/>
<blockquote>
<p>[!Important]</p>
<p>Il pacchetto <a href="microsoft-kerberos.md">Microsoft Kerberos</a> non supporta i contesti di datagramma in modalità utente-utente.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Un contesto orientato al flusso è responsabile del blocco e della formattazione dei messaggi all'interno del pacchetto di sicurezza. Il chiamante non è interessato alla formattazione, ma piuttosto a un flusso di dati non elaborato.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Requisiti del contesto](context-requirements.md)
</dt> <dt>

[Contesti orientati alla connessione](connection-oriented-contexts.md)
</dt> <dt>

[Contesti di datagramma](datagram-contexts.md)
</dt> <dt>

[Contesti di flusso](stream-contexts.md)
</dt> </dl>

 

 
