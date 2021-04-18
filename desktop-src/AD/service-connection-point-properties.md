---
title: Proprietà del punto di connessione del servizio
description: Gli attributi della classe serviceConnectionPoint sono sufficienti per la maggior parte dei servizi.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Proprietà del punto di connessione del servizio
- Active Directory punti di connessione del servizio, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511bbba8acf50a185f1bdd8b55d9b7f8ce684817
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104117534"
---
# <a name="service-connection-point-properties"></a>Proprietà del punto di connessione del servizio

Gli attributi della classe **serviceConnectionPoint** sono sufficienti per la maggior parte dei servizi. Active Directory Domain Services non definiscono il modo in cui vengono usati gli attributi, quindi i client del servizio devono essere in grado di interpretare e usare i dati nel servizio convergenza. I servizi che devono pubblicare dati aggiuntivi su se stessi possono estendere lo schema di Active Directory creando una sottoclasse della classe **serviceConnectionPoint** , assegnando alla sottoclasse un nome distinto. Per ulteriori informazioni sulle estensioni dello schema, vedere [estensione dello schema](extending-the-schema.md).

Gli attributi più importanti di un SCP sono **Keywords**, **serviceDNSName**, **serviceDNSNameType**, **serviceClassName** e **serviceBindingInformation**. Le applicazioni client cercano i valori delle **parole chiave** nella directory per individuare il punto di SCP. Quando viene trovato l'SCP, i client possono leggere altri attributi per recuperare i dati del servizio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Parole</strong><br/></td>
<td>L'attributo <strong>Keywords</strong> può contenere più valori stringa che identificano il servizio. Questo attributo è incluso nel catalogo globale, il che significa che i client in qualsiasi dominio di una foresta aziendale possono eseguire ricerche nel catalogo globale per le parole chiave associate al servizio. Questo attributo è inoltre indicizzato, che consente di migliorare le prestazioni di esecuzione delle query. Il programma di installazione che crea il SCP imposta i valori dell'attributo <strong>Keywords</strong> . In genere, questi valori non vengono modificati dal servizio attivo.<br/> Le parole chiave esatte da includere nell'SCP dipendono dal modo in cui i client cercano il servizio. Le parole chiave migliori da usare sono stringhe GUID perché i GUID sono sicuramente univoci in una foresta. Usare il formato stringa GUID restituito dalla funzione <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> nella libreria RPC. È anche possibile includere nomi leggibili, se possono essere usati dai client per cercare il servizio. Le parole chiave in un SCP devono includere stringhe GUID e/o nomi che identificano i dati seguenti relativi al servizio:
<ul>
<li>Azienda o organizzazione: ad esempio, fabrikam.</li>
<li>Prodotto o servizio: ad esempio, SQL Server. Ciò consente alle applicazioni client di trovare convergenza per i servizi di quel tipo.</li>
<li>Versione specifica del prodotto o del servizio, ad esempio 7,5.</li>
<li>Per convergenza che pubblicano un set specifico di dati o funzionalità per un tipo di servizio, includere una stringa GUID o un nome che identifichi l'istanza specifica. Ad esempio, un servizio di database potrebbe pubblicare un SCP per un database specifico. In questo caso, SCP include un GUID di prodotto per identificare il servizio e un altro GUID per identificare il database.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>serviceDNSName</strong> e <strong>serviceDNSNameType</strong><br/></td>
<td>Le applicazioni client utilizzano gli attributi <strong>serviceDNSName</strong> e <strong>serviceDNSNameType</strong> per determinare il computer host del servizio. Il valore <strong>serviceDNSNameType</strong> indica il tipo di nome DNS specificato da <strong>serviceDNSName</strong> in &quot; genere &quot; se <strong>serviceDNSName</strong> contiene un nome host o &quot; SRV &quot; se <strong>serviceDNSName</strong> contiene un nome di record SRV.<br/> Il valore <strong>serviceDNSName</strong> è in genere il nome DNS del computer host del servizio. Il programma di installazione del servizio può chiamare la funzione <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>presunto GetComputerNameEx</strong></a> per ottenere il nome DNS del computer locale.<br/> Per i servizi che dispongono di record SRV DNS, <strong>serviceDNSName</strong> può essere il nome del record SRV. Un'applicazione client usa le API DNS per recuperare tutti i record SRV che corrispondono a questo nome. Il client recupera quindi il nome host DNS da uno dei record SRV. Questa tecnica è utile per i servizi replicati perché i record SRV includono anche dati che consentono al client di selezionare la replica migliore.<br/></td>
</tr>
<tr class="odd">
<td><strong>serviceBindingInformation</strong><br/></td>
<td>Proprietà multivalore che contiene valori stringa che archiviano i dati necessari per l'associazione a un servizio. Questa proprietà è indicizzata e viene replicata nel catalogo globale.<br/> Il contenuto di <strong>serviceBindingInformation</strong> è specifico del servizio che ha pubblicato SCP; i client devono interpretare i dati di associazione. Nel caso più comune, i dati dell'associazione sono costituiti da un numero di porta nel computer host del servizio.<br/></td>
</tr>
<tr class="even">
<td><strong>serviceClassName</strong><br/></td>
<td>Proprietà a valore singolo che identifica la classe di servizio rappresentata dal SCP. Si tratta di una stringa descrittiva specifica per il servizio che ha pubblicato SCP; ad esempio, SqlServer. Per i servizi che supportano l'autenticazione reciproca, i client possono usare questa proprietà, insieme al nome DNS del computer host del servizio, per formare un nome dell'entità servizio. Per ulteriori informazioni, vedere <a href="mutual-authentication-using-kerberos.md">l'autenticazione reciproca tramite Kerberos</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

