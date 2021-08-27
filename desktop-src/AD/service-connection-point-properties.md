---
title: Proprietà del punto di connessione del servizio
description: Gli attributi della classe serviceConnectionPoint sono sufficienti per la maggior parte dei servizi.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Proprietà del punto di connessione del servizio
- punti di connessione del servizio AD , proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1343833d1a61e4df6dfc44238f9f094b00844f0b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473487"
---
# <a name="service-connection-point-properties"></a>Proprietà del punto di connessione del servizio

Gli attributi della classe **serviceConnectionPoint** sono sufficienti per la maggior parte dei servizi. Active Directory Domain Services definire come vengono usati gli attributi, pertanto i client del servizio devono essere in grado di interpretare e usare i dati nei provider di servizi. I servizi che devono pubblicare dati aggiuntivi su se stessi possono estendere lo schema di Active Directory creando una sottoclasse della classe **serviceConnectionPoint,** fornendo alla sottoclasse un nome distinto. Per altre informazioni sulle estensioni dello schema, vedere [Estensione dello schema](extending-the-schema.md).

Gli attributi più importanti di un SCP sono **le** parole chiave **, serviceDNSName**, **serviceDNSNameType**, **serviceClassName** e **serviceBindingInformation**. Le applicazioni client ricercano nella directory i **valori delle parole** chiave per individuare il pc SCP. Quando viene trovato il SCP, i client possono leggere altri attributi per recuperare i dati del servizio.




| Attributo | Descrizione | 
|-----------|-------------|
| <strong>Parole chiavi</strong><br /> | <strong>L'attributo keywords</strong> può contenere più valori stringa che identificano il servizio. Questo attributo è incluso nel catalogo globale, ovvero i client in qualsiasi dominio di una foresta aziendale possono cercare nel Catalogo globale parole chiave associate al servizio. Anche questo attributo viene indicizzato, migliorando le prestazioni delle query. Il programma di installazione che crea SCP imposta i valori dell'attributo <strong>keywords.</strong> In genere, questi valori non vengono modificati dal servizio attivo.<br /> Le parole chiave esatte da includere nel pc SCP dipendono dalla modalità di ricerca del servizio da parte dei client. Le parole chiave migliori da usare sono le stringhe GUID perché i GUID sono sempre univoci in una foresta. Usare il formato stringa GUID restituito <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>dalla funzione UuidToString</strong></a> nella libreria RPC. È anche possibile includere nomi leggibili, se i client possono usarli per cercare il servizio. Le parole chiave in un SCP devono includere stringhe GUID e/o nomi che identificano i dati seguenti relativi al servizio:<ul><li>Azienda o organizzazione, ad esempio Fabrikam.</li><li>Prodotto o servizio: ad esempio, SQL Server. In questo modo le applicazioni client possono trovare gli scp per i servizi di quel tipo.</li><li>Versione specifica del prodotto o del servizio, ad esempio 7.5.</li><li>Per i provider di servizi di configurazione che pubblicano un set specifico di dati o funzionalità per un tipo di servizio, includere una stringa GUID o un nome che identifica l'istanza specifica. Ad esempio, un servizio di database può pubblicare un SCP per un database specifico. In questo caso, SCP include un GUID del prodotto per identificare il servizio e un altro GUID per identificare il database.</li></ul><br /> | 
| <strong>serviceDNSName</strong> e <strong>serviceDNSNameType</strong><br /> | Le applicazioni client usano <strong>gli attributi serviceDNSName</strong> e <strong>serviceDNSNameType</strong> per determinare il computer host del servizio. Il <strong>valore serviceDNSNameType</strong> indica il tipo di nome DNS specificato da <strong>serviceDNSName</strong> in genere "A" se <strong>serviceDNSName</strong> contiene un nome host o "SRV" se <strong>serviceDNSName</strong> contiene un nome di record SRV.<br /> Il <strong>valore serviceDNSName</strong> è in genere il nome DNS del computer host del servizio. Il programma di installazione del servizio può chiamare <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>la funzione GetComputerNameEx</strong></a> per ottenere il nome DNS del computer locale.<br /> Per i servizi con record DNS SRV, <strong>serviceDNSName</strong> può essere il nome del record SRV. Un'applicazione client usa le API DNS per recuperare tutti i record SRV che corrispondono a questo nome. Il client recupera quindi il nome host DNS da uno dei record SRV. Questa tecnica è utile per i servizi replicati perché i record SRV includono anche dati che consentono al client di selezionare la replica migliore.<br /> | 
| <strong>serviceBindingInformation</strong><br /> | Proprietà multivalore che contiene valori stringa che archiviano i dati necessari per l'associazione a un servizio. Questa proprietà è indicizzata e replicata nel catalogo globale.<br /> Il contenuto di <strong>serviceBindingInformation</strong> è specifico del servizio che ha pubblicato il protocollo SCP. I client devono interpretare i dati di associazione. Nel caso più comune, i dati di associazione sono costituiti da un numero di porta nel computer host del servizio.<br /> | 
| <strong>serviceClassName</strong><br /> | Proprietà a valore singolo che identifica la classe di servizio rappresentata da SCP. Si tratta di una stringa descrittiva specifica del servizio che ha pubblicato il protocollo SCP. ad esempio SqlServer. Per i servizi che supportano l'autenticazione reciproca, i client possono usare questa proprietà, insieme al nome DNS del computer host del servizio, per formare un nome dell'entità servizio. Per altre informazioni, vedere <a href="mutual-authentication-using-kerberos.md">Autenticazione reciproca tramite Kerberos.</a><br /> | 




 

 

