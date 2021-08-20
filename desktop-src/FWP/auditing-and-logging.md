---
title: Controllo
description: Windows La piattaforma di filtro (WFP) consente di controllare gli eventi correlati a firewall e IPsec.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 854841685bab015fc0b9a4bc985762df46a7f0c89eae3d38b4b63e081107b70b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015409"
---
# <a name="auditing"></a>Controllo

La Windows Filtering Platform (WFP) fornisce il controllo degli eventi correlati a firewall e IPsec. Questi eventi vengono archiviati nel registro di sicurezza di sistema.

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
<td>Applicazione di filtri alla modifica dei criteri della piattaforma<br/> {0CCE9233-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
I numeri rappresentano gli ID evento visualizzati da Visualizzatore eventi (eventvwr.exe).
</blockquote>
<br/> Aggiunta e rimozione di oggetti WFP:<br/>
<ul>
<li>5440 Callout permanente aggiunto</li>
<li>5441 Boot-time or persistent filter added (5441 Boot-time or persistent filter added)</li>
<li>5442 Provider permanente aggiunto</li>
<li>5443 Aggiunta del contesto del provider permanente</li>
<li>5444 Livello secondario permanente aggiunto</li>
<li>5446 Callout run-time aggiunto o rimosso</li>
<li>5447 Filtro di run-time aggiunto o rimosso</li>
<li>5448 Provider di run-time aggiunto o rimosso</li>
<li>5449 Contesto del provider di run-time aggiunto o rimosso</li>
<li>5450 Sottostrato run-time aggiunto o rimosso</li>
</ul></td>
</tr>
<tr class="even">
<td>Accesso a oggetti<br/> {6997984A-797A-11D9-BED3-505054503030}<br/></td>
<td>Filtro dell'eliminazione dei pacchetti della piattaforma <br/> {0CCE9225-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacchetti eliminati dal WFP:<br/>
<ul>
<li>5152 Pacchetto eliminato</li>
<li>5153 Packet vetoed</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accesso a oggetti<br/></td>
<td>Filtro della connessione alla piattaforma <br/> {0CCE9226-69AE-11D9-BED3-505054503030}<br/></td>
<td>Connessioni consentite e bloccate:<br/>
<ul>
<li>5154 Ascolto consentito</li>
<li>5155 Ascolto bloccato</li>
<li>5156 Connessione consentita</li>
<li>5157 Connessione bloccata</li>
<li>5158 Binding consentito</li>
<li>5159 Binding bloccato</li>
</ul>
<blockquote>
[!Note]<br />
Le connessioni consentite non controllano sempre l'ID del filtro associato. FilterID per TCP sarà 0 a meno che non venga usato un subset di queste condizioni di filtro: UserID, AppID, Protocol, Remote Port.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Accesso a oggetti<br/></td>
<td>Altri eventi di accesso agli oggetti<br/> {0CCE9227-69AE-11D9-BED3-505054503030}<br/></td>
<td><blockquote>
[!Note]<br />
Questa sottocategoria abilita molti controlli. I controlli specifici del WFP sono elencati di seguito.
</blockquote>
<br/> Stato di prevenzione Denial of Service:<br/>
<ul>
<li>5148 Modalità di prevenzione DoS del WFP avviata</li>
<li>5149 Wfp DoS prevention mode stopped</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accesso/Disconnessione<br/> {69979849-797A-11D9-BED3-505054503030}<br/></td>
<td>Modalità principale IPsec<br/> {0CCE9218-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negoziazione in modalità principale IKE e AuthIP:<br/>
<ul>
<li>4650, 4651 Associazione di sicurezza stabilita</li>
<li>4652, 4653 Negoziazione non riuscita</li>
<li>4655 Associazione di sicurezza terminata</li>
</ul></td>
</tr>
<tr class="even">
<td>Accesso/Disconnessione<br/></td>
<td>Modalità rapida IPsec <br/> {0CCE9219-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negoziazione in modalità rapida IKE e AuthIP:<br/>
<ul>
<li>5451 Associazione di sicurezza stabilita</li>
<li>5452 Associazione di sicurezza terminata</li>
<li>4654 Negoziazione non riuscita</li>
</ul></td>
</tr>
<tr class="odd">
<td>Accesso/Disconnessione <br/></td>
<td>Modalità estesa IPsec<br/> {0CCE921A-69AE-11D9-BED3-505054503030}<br/></td>
<td>Negoziazione in modalità estesa AuthIP:<br/>
<ul>
<li>4978 Pacchetto di negoziazione non valido</li>
<li>4979, 4980, 4981, 4982 Associazione di sicurezza stabilita</li>
<li>4983, 4984 Negoziazione non riuscita</li>
</ul></td>
</tr>
<tr class="even">
<td>Sistema<br/> {69979848-797A-11D9-BED3-505054503030}<br/></td>
<td>IPsec Driver<br/> {0CCE9213-69AE-11D9-BED3-505054503030}<br/></td>
<td>Pacchetti eliminati dal driver IPsec:<br/>
<ul>
<li>4963 Pacchetto di testo non crittografato in ingresso eliminato</li>
</ul></td>
</tr>
</tbody>
</table>



 

Per impostazione predefinita, il controllo per WFP è disabilitato.

Il controllo può essere abilitato per ogni categoria tramite lo snap-in MMC Editor oggetti Criteri di gruppo, lo snap-in MMC Criteri di sicurezza locali o il auditpol.exe comando.

Ad esempio, per abilitare il controllo degli eventi di modifica dei criteri, è possibile:

-   Usare il Editor oggetti Criteri di gruppo

    1.  Eseguire **gpedit.msc**.
    2.  Espandere Criteri computer locale.
    3.  Espandere Configurazione computer.
    4.  Espandere Windows Impostazioni.
    5.  Espandere Sicurezza Impostazioni.
    6.  Espandere Criteri locali.
    7.  Fare clic su Criteri di controllo.
    8.  Fare doppio clic su Controlla modifica criteri per avviare la finestra di dialogo Proprietà.
    9.  Selezionare le caselle di controllo Operazioni riuscite e Non riuscite.

-   Usare i criteri di sicurezza locali

    1.  Eseguire **secpol.msc**.
    2.  Espandere Criteri locali.
    3.  Fare clic su Criteri di controllo.
    4.  Fare doppio clic su Controlla modifica criteri per avviare la finestra di dialogo Proprietà.
    5.  Selezionare le caselle di controllo Operazioni riuscite e Non riuscite.

-   Usare il auditpol.exe comando

    -   **auditpol /set /category:"Policy Change" /success:enable /failure:enable**

Il controllo può essere abilitato per ogni sottocategoria solo tramite il auditpol.exe comando .

I nomi delle categorie e delle sottocategorie di controllo sono localizzati. Per evitare la localizzazione per gli script di controllo, è possibile usare i GUID corrispondenti al posto dei nomi.

Ad esempio, per abilitare il controllo degli eventi di modifica dei criteri della piattaforma di filtro, è possibile usare uno dei comandi seguenti:

-   **auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**
-   **auditpol /set /subcategory:"{0CCE9233-69AE-11D9-MENU3-505054503030}" /success:enable /failure:enable**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))
</dt> <dt>

[Registro eventi](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))
</dt> <dt>

[Criteri di gruppo](/windows/deployment/deploy-whats-new)
</dt> </dl>

