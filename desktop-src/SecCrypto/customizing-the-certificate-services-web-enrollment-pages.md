---
description: Servizi certificati fornisce pagine di registrazione Web che possono essere usate per richiedere i certificati.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Personalizzazione delle pagine di registrazione Web di Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb2fbf421eceb1ebf0b15379aca5d0788a992ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885073"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Personalizzazione delle pagine di registrazione Web di Servizi certificati

[*Servizi certificati*](../secgloss/c-gly.md) fornisce pagine di registrazione Web che possono essere usate per richiedere i certificati. Un amministratore può personalizzare alcuni elementi che possono essere visualizzati nelle pagine di registrazione Web; è tuttavia necessario acquisire familiarità con le pagine di registrazione Web e gli script Web prima di apportare qualsiasi modifica. Per ulteriori informazioni sugli script Web, vedere [Scripting](/previous-versions/ms950396(v=msdn.10)).

I valori predefiniti per i campi del nome distinto per organizzazione, unità organizzativa, località, stato e paese/area geografica sono i valori specificati per l' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) quando è installato Servizi certificati. Questi valori predefiniti vengono visualizzati nelle pagine Web e possono essere modificati dall'utente durante il processo di registrazione del certificato. Tuttavia, se si desidera che vengano visualizzati altri valori predefiniti nelle pagine Web, è possibile modificare il file file Certdat. Inc (nel percorso \\ *WindowsDirectory* \\ system32 \\ certsrv \\ ); in particolare, è possibile assegnare valori personalizzati alle seguenti variabili fornite per la personalizzazione.



| Variabile            | Descrizione                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Società predefinita (viene visualizzata nella [*richiesta di certificato*](../secgloss/c-gly.md) come campo dell'organizzazione [*X. 509*](../secgloss/x-gly.md) ). |
| sDefaultOrgUnit     | Reparto predefinito (viene visualizzato nella richiesta di certificato come campo dell'unità organizzativa X. 509).                                                                                                                                           |
| sDefaultLocality    | Città predefinita (viene visualizzata nella richiesta di certificato come campo del percorso X. 509).                                                                                                                                                            |
| sDefaultState       | Stato predefinito/provincia (visualizzato nella richiesta certificato come campo stato X. 509).                                                                                                                                                     |
| sDefaultCountry     | Paese/area geografica predefinito (visualizzato nella richiesta di certificato come campo del paese/area geografica X. 509).                                                                                                                                            |
| nPendingTimeoutDays | Numero di giorni in cui l'utente può recuperare un certificato in sospeso dopo che è stato richiesto.                                                                                                                                          |



 

Non è necessario modificare altre variabili nel file file Certdat. Inc.

Nell'esempio seguente viene impostata l'unità organizzativa predefinita su "marketing".


```VB
sDefaultOrgUnit="Marketing"
```



Inoltre, è possibile modificare il file Certrqtp. Inc per aggiungere, modificare o rimuovere i [*modelli*](../secgloss/c-gly.md) o i tipi di certificato disponibili per l'utente. Questi modelli e tipi, nonché le informazioni correlate, sono contenuti in una matrice con dimensione denominata rgAvailReqTypes (*m*, 5).

Questa matrice, come tutte Visual Basic matrici di Scripting Edition, è basata su zero e, di conseguenza, la prima dimensione della matrice, *m*, alloca memoria per *m*+ 1 elementi. Se quindi si personalizzano le pagine Web, è necessario modificare il numero di elementi nella matrice rgAvailReqTypes, impostare la dimensione *m* su un valore inferiore al numero totale di elementi necessari. Se, ad esempio, si dispone di sette modelli di certificato, modificare la dichiarazione di rgAvailReqTypes come illustrato nell'esempio seguente.


```VB
Dim rgAvailReqTypes(6,5)
```



La seconda dimensione della matrice, che ha sempre il valore cinque, alloca i sei campi che compongono ogni elemento. Questi sei campi rappresentano il modello o il tipo di certificato, il nome visualizzato associato a questo modello o tipo e se il modello richiede [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME).

Per semplificare la comprensione dei campi a cui si accede, Certrqtp. Inc fornisce anche le costanti seguenti che è possibile usare per l'impostazione di valori di campo.



| Costante                              | Descrizione                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_OID campo**                        | (Si applica a CA autonome) Indicizzare il primo campo dell'elemento; rappresenta un [*identificatore di oggetto*](../secgloss/o-gly.md) (OID) per un tipo di certificato.<br/>                                                                                                           |
| **modello di campo \_**                   | (Si applica alle CA globali (Enterprise)) Indicizzare il primo campo dell'elemento; rappresenta un modello di certificato.<br/>                                                                                                                                                                                                                           |
| **\_FriendlyName Field**               | Indice per il secondo campo dell'elemento; rappresenta il nome visualizzato (che l'utente visualizzerà durante la registrazione) dell'elemento nel primo campo.                                                                                                                                                                                               |
| **CAMPO \_ CSPLIST**                    | Indice al terzo campo dell'elemento. Elenco di nomi di [*provider del servizio di crittografia*](../secgloss/c-gly.md) consentiti dal modello. Ogni nome nell'elenco è separato da un punto interrogativo (?).                                                    |
| **CAMPO \_ CSPLIST2**                   | Indice al quarto campo dell'elemento. Elenco secondario di nomi di [*provider del servizio di crittografia*](../secgloss/c-gly.md) consentiti dal modello. Ogni nome nell'elenco è separato da un punto interrogativo (?). Questo elenco fornisce un valore predefinito diverso. |
| **CAMPO \_ esportabile**                 | Indice del quinto campo dell'elemento. Indica se il modello specifica che la chiave deve essere esportabile. Se questo campo contiene "true", la chiave può essere esportata. Se questo campo contiene "false", la chiave non è esportabile.                                                                                                        |
| **il \_ campo \_ richiede \_ funzionalità SMIME** | Questa costante non è supportata.                                                                                                                                                                                                                                                                                                      |



 

Ad esempio, le espressioni seguenti assegnano l'OID di 1.3.6.1.5.5.7.3.2 al primo campo del primo elemento e assegnano "Web browser certificate" al secondo campo del primo elemento. il valore della matrice di zero indicizza il primo elemento.


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



Il risultato di queste assegnazioni è che l'utente visualizzerà il **certificato del Web browser** durante la registrazione. se l'utente seleziona il **certificato del Web browser**, la [*richiesta di certificato*](../secgloss/c-gly.md) conterrà l'OID 1.3.6.1.5.5.7.3.2.

Il file Certrqtp. Inc contiene anche le costanti usate per i nomi visualizzati dei modelli o dei tipi di certificato. Nell'esempio seguente viene illustrato il formato.


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Queste costanti sono definite in un blocco nel file Certrqtp. Inc e questo raggruppamento rende più semplice assegnare a ognuno di essi un valore personalizzato. Questa operazione è particolarmente utile quando si localizzano i nomi visualizzati per le versioni internazionali delle pagine Web.

Infine, il file Certrqtp. Inc contiene una variabile che rappresenta il numero di modelli di certificato o tipi nella matrice rgAvailReqTypes. Diversamente dalla dimensione *m* della matrice, impostare il valore della variabile nAvailReqTypes sul numero effettivo di modelli o tipi di certificato che l'installazione utilizzerà. il valore non deve essere maggiore di *m*+ 1. Sebbene dichiarati nella parte superiore del file Certrqtp. Inc, a nAvailReqTypes viene assegnato un valore dopo che la matrice rgAvailReqTypes è stata popolata, semplificando la visualizzazione del numero di elementi effettivamente utilizzati dalla matrice. Il valore nAvailReqTypes viene usato in un'iterazione altrove nelle pagine di registrazione Web, pertanto è importante che questa variabile rifletta accuratamente il numero di modelli di certificato o di tipi che si desidera visualizzare all'utente.

Si noti che l'aggiunta di [*modelli di certificato*](../secgloss/c-gly.md) e tipi al file Certrqtp. Inc non garantisce che l'utente possa ottenere un certificato con tali tratti; la CA deve essere autorizzata a emettere un certificato per il tipo o il modello di certificato specificato.

Le installazioni possono creare le proprie applicazioni o pagine Web per richiedere e ricevere un certificato. Gli oggetti [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) e [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) consentono ai programmatori o ai creatori di script di compilare applicazioni di [*richiesta di certificati*](../secgloss/c-gly.md) .

Per richiedere l'emissione di un certificato su una [*Smart Card*](../secgloss/s-gly.md), è possibile usare il controllo di registrazione delle smart card. Per informazioni dettagliate e codice di esempio, vedere [**ISCrdEnr**](iscrdenr.md).

 

 
