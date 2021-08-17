---
description: È possibile fornire tutte le informazioni necessarie per configurare Installazione applicazioni in Pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto del programma di installazione Windows dell'applicazione.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurazione di Installazione applicazioni con il programma di Windows installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99e1393eb586cfe1067840e4622fddd777a84512f55f9e82f7c9fad3b1f5688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638750"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configurazione di Installazione applicazioni con il programma di Windows installazione

È possibile fornire tutte le informazioni necessarie per configurare Installazione applicazioni in Pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto del programma di installazione Windows dell'applicazione. L'impostazione di queste proprietà scrive automaticamente i valori corrispondenti nel Registro di sistema. Se il programma di installazione rileva che il prodotto è contrassegnato per la rimozione completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere la cartella Installazione applicazioni Pannello di controllo informazioni sul prodotto.

Se un'applicazione non è registrata, non è elencata in Installazione applicazioni in Pannello di controllo. Per altre informazioni, vedere [Aggiunta e rimozione di un'applicazione e Assenza di traccia nel Registro di sistema.](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)

Le applicazioni installate nel contesto [](installation-context.md) di installazione per utente vengono visualizzate in Installazione applicazioni dell'utente corrente. Le applicazioni installate nel contesto di installazione per computer vengono visualizzate in Installazione applicazioni di tutti gli utenti. Le applicazioni che non sono state installate per computer e sono state installate solo come applicazioni per utente per utenti diversi dall'utente corrente, non vengono visualizzate in Installazione applicazioni dell'utente corrente.

Si noti che i pacchetti di installazione che usano la [**proprietà LIMITUI**](limitui.md) devono contenere anche [**ARPNOMODIFY**](arpnomodify.md). Questa operazione è necessaria per ottenere il comportamento corretto da Installazione applicazioni nell'utilità Pannello di controllo quando si tenta di configurare un prodotto.

Il programma di installazione usa [le proprietà pubbliche seguenti](public-properties.md) per gestire Installazione applicazioni in Pannello di controllo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome proprietà</th>
<th>Breve descrizione della proprietà</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></td>
<td>URL del canale di aggiornamento per l'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Fornisce commenti per Installazione applicazioni nel Pannello di controllo. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Fornisce il contatto per Installazione applicazioni nel Pannello di controllo. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Percorso completo della cartella primaria dell'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Indirizzo Internet, o URL, per il supporto tecnico. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Numeri di telefono del supporto tecnico. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Impedisce la visualizzazione di un pulsante Cambia per il prodotto in Installazione applicazioni nel Pannello di controllo.
<blockquote>
<b>Nota:</b> Ciò influisce solo sulla visualizzazione nel componente ARP. Il Windows installer è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Impedisce la visualizzazione di un pulsante Rimuovi per il prodotto in Installazione applicazioni nel Pannello di controllo. Il prodotto può comunque essere rimosso selezionando il pulsante Cambia se il pacchetto di installazione è stato creato con un'interfaccia utente che fornisce la rimozione del prodotto come opzione.
<blockquote>
<b>Nota:</b> Ciò influisce solo sulla visualizzazione nel componente ARP. Il Windows installer è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Disabilita il pulsante Ripristina in Installazione applicazioni nel Pannello di controllo.
<blockquote>
<b>Nota:</b> Ciò influisce solo sulla visualizzazione nel componente ARP. Il Windows installer è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifica l'icona visualizzata in Installazione applicazioni. Se questa proprietà non è definita, Installazione applicazioni specifica l'icona di visualizzazione.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Fornisce il file Leggimi per Installazione applicazioni in Pannello di controllo. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Dimensioni stimate dell'applicazione in KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Impedisce la visualizzazione dell'applicazione nell'elenco programmi di Installazione applicazioni nel Pannello di controllo.
<blockquote>
<b>Nota:</b> Ciò influisce solo sulla visualizzazione nel componente ARP. Il Windows installer è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>URL per l'home page dell'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>URL per le informazioni sull'aggiornamento dell'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">disinstalla del Registro di sistema</a>.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Per informazioni sullo strumento Imposta programma e impostazioni predefinite, vedere la sezione Utilizzo dell'accesso ai programmi e delle impostazioni [predefinite del computer.](/previous-versions//bb776877(v=vs.85))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disinstallare la chiave del Registro di sistema](uninstall-registry-key.md)
</dt> </dl>
