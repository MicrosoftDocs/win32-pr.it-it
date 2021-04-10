---
title: Controllo
description: Windows Filtering Platform (WFP) fornisce il controllo degli eventi correlati a firewall e IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "103963625"
---
# <a name="auditing"></a>Controllo

Windows Filtering Platform (WFP) fornisce il controllo degli eventi correlati a firewall e IPsec. Questi eventi vengono archiviati nel registro di sicurezza del sistema.

Gli eventi controllati sono i seguenti.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoria di controllo</th>
<th>Sottocategoria di controllo</th>
<th>Eventi controllati</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Modifica dei criteri<br/> {6997984D-797A-11D9-BED3-505054503030}<br/></td>
<td>Modifica dei criteri della piattaforma di filtro<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
I numeri rappresentano gli ID evento visualizzati da Visualizzatore eventi (eventvwr.exe).
</blockquote>
<br/> Aggiunta e rimozione di oggetti WFP:<br/>
<ul>
<li>5440 callout permanente aggiunto</li>
<li>5441 tempo di avvio o filtro permanente aggiunto</li>
<li>5442 provider persistente aggiunto</li>
<li>5443 contesto del provider persistente aggiunto</li>
<li>5444 sottolivello permanente aggiunto</li>
<li>5446 callout di run-time aggiunto o rimosso</li>
<li>5447 filtro di runtime aggiunto o rimosso</li>
<li>5448 provider di runtime aggiunto o rimosso</li>
<li>5449 contesto del provider di runtime aggiunto o rimosso</li>
<li>5450 sottolivello runtime aggiunto o rimosso</li>
</ul></td>
</tr>
<tr class="even">
<td>Accesso a oggetti<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Eliminazione di pacchetti di piattaforma di filtro <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacchetti eliminati da WFP:<br/>
<ul>
<li>pacchetto 5152 rilasciato</li>
<li>pacchetto 5153 con veto</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accesso a oggetti<br/></td>
<td>Connessione alla piattaforma di filtro <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Connessioni consentite e bloccate:<br/>
<ul>
<li>5154 ascolto consentito</li>
<li>5155 ascolto bloccato</li>
<li>connessione 5156 consentita</li>
<li>connessione 5157 bloccata</li>
<li>5158 associazione consentita</li>
<li>5159 binding bloccato</li>
</ul>
<blockquote>
[!Note]<br />
Le connessioni consentite non controllano sempre l'ID del filtro associato. Il valore di FilterID per TCP sarà 0, a meno che non venga utilizzato un subset di queste condizioni di filtro: UserID, AppID, protocollo, porta remota.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Accesso a oggetti<br/></td>
<td>Altri eventi di accesso agli oggetti<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Questa sottocategoria Abilita molti controlli. I controlli specifici del WFP sono elencati di seguito.
</blockquote>
<br/> Stato di prevenzione di attacchi Denial of Service:<br/>
<ul>
<li>5148 modalità di prevenzione DoS PAM avviata</li>
<li>5149 modalità di prevenzione DoS PAM arrestata</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accesso/disconnessione<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Modalità principale IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negoziazione in modalità principale IKE e AuthIP:<br/>
<ul>
<li>4650, associazione di sicurezza 4651 stabilita</li>
<li>4652, negoziazione 4653 non riuscita</li>
<li>4655 associazione di sicurezza terminata</li>
</ul></td>
</tr>
<tr class="even">
<td>Accesso/disconnessione<br/></td>
<td>Modalità rapida IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negoziazione in modalità rapida IKE e AuthIP:<br/>
<ul>
<li>5451 associazione di sicurezza stabilita</li>
<li>5452 associazione di sicurezza terminata</li>
<li>negoziazione 4654 non riuscita</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accesso/disconnessione <br/></td>
<td>Modalità estesa IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negoziazione in modalità estesa AuthIP:<br/>
<ul>
<li>4978 pacchetto di negoziazione non valido</li>
<li>4979, 4980, 4981, 4982 associazione di sicurezza stabilita</li>
<li>4983, negoziazione 4984 non riuscita</li>
</ul></td>
</tr>
<tr class="even">
<td>Sistema<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>Driver IPsec<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacchetti eliminati dal driver IPsec:<br/>
<ul>
<li>4963 pacchetto di testo non crittografato in ingresso eliminato</li>
</ul></td>
</tr>
</tbody>
</table>



 

Per impostazione predefinita, il controllo per WFP è disabilitato.

Il controllo può essere abilitato per ogni categoria tramite lo snap-in Editor oggetti Criteri di gruppo MMC, lo snap-in MMC Criteri di sicurezza locali o il comando auditpol.exe.

Ad esempio, per abilitare il controllo degli eventi di modifica dei criteri, è possibile:

-   Usare il Editor oggetti Criteri di gruppo

    1.  Eseguire **gpedit. msc**.
    2.  Espandere criteri del computer locale.
    3.  Espandere Configurazione computer.
    4.  Espandere impostazioni di Windows.
    5.  Espandere impostazioni di sicurezza.
    6.  Espandere Criteri locali.
    7.  Fare clic su criteri di controllo.
    8.  Fare doppio clic su Controlla modifiche dei criteri per avviare la finestra di dialogo Proprietà.
    9.  Controllare le caselle di controllo di esito positivo e negativo.

-   Usare i criteri di sicurezza locali

    1.  Eseguire **secpol. msc**.
    2.  Espandere Criteri locali.
    3.  Fare clic su criteri di controllo.
    4.  Fare doppio clic su Controlla modifiche dei criteri per avviare la finestra di dialogo Proprietà.
    5.  Controllare le caselle di controllo di esito positivo e negativo.

-   Usare il comando auditpol.exe

    -   **auditpol/set/category: "modifica dei criteri"/Success: enable/failure: Enable**

Il controllo può essere abilitato in base alla sottocategoria solo tramite il comando auditpol.exe.

I nomi di categoria e sottocategoria di controllo sono localizzati. Per evitare la localizzazione per gli script di controllo, è possibile usare i GUID corrispondenti al posto dei nomi.

Ad esempio, per abilitare il controllo degli eventi di modifica dei criteri della piattaforma di filtro è possibile usare uno dei comandi seguenti:

-   **auditpol/set/SubCategory: "Filtering Platform policy change"/Success: enable/failure: Enable**
-   **auditpol/set/SubCategory: "{0CCE9233-69AE-11D9-BED3-505054503030}"/Success: enable/failure: Enable**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Registro eventi](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Criteri di gruppo](/windows/deployment/deploy-whats-new)
</dt> </dl>

