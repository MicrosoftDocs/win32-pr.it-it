---
description: Servizi certificati fornisce pagine di registrazione Web che possono essere usate per richiedere certificati.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Personalizzazione delle pagine di registrazione Web di Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0132ce4e5e1fef588ffc429597717433dd1b780d2f7f35f9c886f1978b5b318a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767796"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Personalizzazione delle pagine di registrazione Web di Servizi certificati

[*Servizi certificati fornisce*](../secgloss/c-gly.md) pagine di registrazione Web che possono essere usate per richiedere certificati. Un amministratore può personalizzare alcuni degli elementi che possono essere visualizzati nelle pagine di registrazione Web. Tuttavia, è necessario avere familiarità con le pagine di registrazione Web e gli script Web prima di apportare modifiche. Per altre informazioni sugli script Web, vedere [Scripting](/previous-versions/ms950396(v=msdn.10)).

I valori predefiniti per i campi Nome distinto per Organizzazione, Unità organizzativa, Locality, [](../secgloss/c-gly.md) Stato e Paese/area geografica sono i valori specificati per l'autorità di certificazione (CA) durante l'installazione di Servizi certificati. Questi valori predefiniti vengono visualizzati nelle pagine Web e possono essere modificati dall'utente durante il processo di registrazione del certificato. Tuttavia, se si desidera che altri valori predefiniti vengano visualizzati nelle pagine Web, è possibile modificare il file Certdat.inc (nel percorso \\ *WindowsDirectory* \\ System32 \\ Certsrv ); in particolare, è possibile assegnare valori personalizzati alle variabili seguenti fornite per la \\ personalizzazione.



| Variabile            | Descrizione                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Società predefinita (visualizzata nella [*richiesta di certificato*](../secgloss/c-gly.md) come campo Organizzazione [*X.509).*](../secgloss/x-gly.md) |
| sDefaultOrgUnit     | Reparto predefinito (visualizzato nella richiesta di certificato come campo Unità organizzativa X.509).                                                                                                                                           |
| sDefaultLocality    | Città predefinita (visualizzata nella richiesta di certificato come campo Posizione X.509).                                                                                                                                                            |
| sDefaultState       | Stato/provincia predefinito (visualizzato nella richiesta di certificato come campo Stato X.509).                                                                                                                                                     |
| sDefaultCountry     | Paese/area geografica predefinito (visualizzato nella richiesta di certificato come campo Paese/area geografica X.509).                                                                                                                                            |
| nPendingTimeoutDays | Numero di giorni in cui l'utente può recuperare un certificato in sospeso dopo che è stato richiesto.                                                                                                                                          |



 

Non è necessario modificare altre variabili nel file Certdat.inc.

Nell'esempio seguente l'unità organizzativa predefinita viene impostata su "Marketing".


```VB
sDefaultOrgUnit="Marketing"
```



È anche possibile modificare il file Certrqtp.inc per [](../secgloss/c-gly.md) aggiungere, modificare o rimuovere modelli di certificato o tipi disponibili per l'utente. Questi modelli e tipi, oltre alle informazioni correlate, sono contenuti in una matrice dimensionata denominata rgAvailReqTypes(*m*,5).

Questa matrice, come tutte le matrici Visual Basic Scripting Edition, è in base zero e, di conseguenza, la prima dimensione della matrice, *m*, alloca memoria per *m*+1 elementi. Pertanto, se durante la personalizzazione delle pagine Web è necessario modificare il numero di elementi nella matrice rgAvailReqTypes, impostare la dimensione *m* su uno in meno del numero totale di elementi necessari. Ad esempio, se si avranno sette modelli di certificato, modificare la dichiarazione di rgAvailReqTypes come illustrato nell'esempio seguente.


```VB
Dim rgAvailReqTypes(6,5)
```



La seconda dimensione della matrice, che ha sempre il valore cinque, alloca i sei campi che compongono ogni elemento. Questi sei campi rappresentano il modello o il tipo di certificato, il nome visualizzato associato a questo modello o tipo e se il modello richiede [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).

Per semplificare la comprensione dei campi a cui si accede, Certrqtp.inc fornisce anche le costanti seguenti che è possibile usare quando si impostano i valori dei campi.



| Costante                              | Descrizione                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FIELD \_ OID**                        | (Si applica alle CA autonome) Indice del primo campo dell'elemento; rappresenta un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) per un tipo di certificato.<br/>                                                                                                           |
| **MODELLO DI \_ CAMPO**                   | (Si applica alle CA aziendali) Indice del primo campo dell'elemento; rappresenta un modello di certificato.<br/>                                                                                                                                                                                                                           |
| **FIELD \_ FRIENDLYNAME**               | Indice del secondo campo dell'elemento; rappresenta il nome visualizzato (che verrà visualizzato dall'utente durante la registrazione) dell'elemento nel primo campo.                                                                                                                                                                                               |
| **FIELD \_ CSPLIST**                    | Indice del terzo campo dell'elemento. Elenco di nomi [*di provider del servizio di*](../secgloss/c-gly.md) crittografia consentiti dal modello. Ogni nome nell'elenco è separato da un punto interrogativo (?).                                                    |
| **CAMPO \_ CSPLIST2**                   | Indice del quarto campo dell'elemento. Elenco secondario di [*nomi di provider del servizio di*](../secgloss/c-gly.md) crittografia consentiti dal modello. Ogni nome nell'elenco è separato da un punto interrogativo (?). Questo elenco fornisce un valore predefinito diverso. |
| **FIELD \_ EXPORTABLE**                 | Indice del quinto campo dell'elemento. Indica se il modello specifica che la chiave deve essere esportabile. Se questo campo contiene "True", la chiave è esportabile. Se questo campo contiene "False", la chiave non è esportabile.                                                                                                        |
| **FIELD \_ RICHIEDE \_ FUNZIONALITÀ \_ SMIME** | Questa costante non è supportata.                                                                                                                                                                                                                                                                                                      |



 

Ad esempio, le espressioni seguenti assegnano l'OID di 1.3.6.1.5.5.7.3.2 al primo campo del primo elemento e assegnano "Certificato Web Browser" al secondo campo del primo elemento (il valore della matrice pari a zero indicizza il primo elemento).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



Il risultato di queste assegnazioni è che l'utente visualizza il testo Certificato web **browser** durante [](../secgloss/c-gly.md) la registrazione e, se l'utente seleziona Certificato **web browser,** la richiesta di certificato conterrà l'OID 1.3.6.1.5.5.7.3.2.

Il file Certrqtp.inc contiene anche costanti utilizzate per i nomi visualizzati dei modelli o dei tipi di certificato. Nell'esempio seguente viene illustrato il formato .


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Queste costanti sono definite in un blocco nel file Certrqtp.inc e questo raggruppamento semplifica l'assegnazione di un valore personalizzato a ognuna di esse. Ciò è particolarmente utile quando si localizzano i nomi visualizzati per le versioni internazionali delle pagine Web.

Infine, il file Certrqtp.inc contiene una variabile che rappresenta il numero di modelli o tipi di certificato nella matrice rgAvailReqTypes. A differenza della dimensione *m* della matrice, impostare il valore della variabile nAvailReqTypes sul numero effettivo di modelli o tipi di certificato che verranno utilizzati dall'installazione; questo valore non deve essere maggiore di *m*+1. Anche se dichiarato nella parte superiore del file Certrqtp.inc, a nAvailReqTypes viene assegnato un valore dopo il popolamento della matrice rgAvailReqTypes, semplificando la visualizzazione del numero di elementi effettivamente usati dalla matrice. Il valore nAvailReqTypes viene usato in un'iterazione altrove nelle pagine di registrazione Web, quindi è importante che questa variabile rifletta in modo accurato il numero di modelli o tipi di certificato che si vuole visualizzare all'utente.

Si noti che [](../secgloss/c-gly.md) la semplice aggiunta di modelli e tipi di certificato al file Certrqtp.inc non garantisce che l'utente sarà in grado di ottenere un certificato con tali caratteristiche; l'autorità di certificazione deve essere autorizzata a rilasciare un certificato per il modello o il tipo di certificato specificato.

Le installazioni possono creare applicazioni o pagine Web personalizzate per richiedere e ricevere un certificato. Gli [**oggetti ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) e [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) consentono ai programmatori o agli scripter di compilare [*applicazioni di richiesta di*](../secgloss/c-gly.md) certificato.

Per richiedere l'emissione di un certificato in [*un smart card*](../secgloss/s-gly.md), è possibile usare il controllo di registrazione smart card. Per informazioni dettagliate e codice di esempio, [**vedere ISCrdEnr.**](iscrdenr.md)

 

 
