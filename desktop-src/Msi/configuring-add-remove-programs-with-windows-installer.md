---
description: È possibile fornire tutte le informazioni necessarie per configurare installazione applicazioni nel pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto di Windows Installer dell'applicazione.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurazione di installazione applicazioni con Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/30/2021
ms.locfileid: "106334296"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configurazione di installazione applicazioni con Windows Installer

È possibile fornire tutte le informazioni necessarie per configurare installazione applicazioni nel pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto di Windows Installer dell'applicazione. L'impostazione di queste proprietà scrive automaticamente i valori corrispondenti nel registro di sistema. Se il programma di installazione rileva che il prodotto è contrassegnato per la rimozione completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere la cartella Aggiungi/Rimuovi programmi nel pannello di controllo informazioni per il prodotto.

Se un'applicazione non è registrata, non è elencata in Installazione applicazioni nel pannello di controllo. Per ulteriori informazioni, vedere [aggiunta e rimozione di un'applicazione senza traccia nel registro di sistema](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).

Le applicazioni installate nel [contesto di installazione](installation-context.md) per utente vengono visualizzate in Installazione applicazioni dell'utente corrente. Le applicazioni che sono state installate nel contesto di installazione per computer vengono visualizzate in Installazione applicazioni di tutti gli utenti. Le applicazioni che non sono state installate per computer e sono state installate solo come applicazioni per utente per utenti diversi dall'utente corrente, non vengono visualizzate nell'installazione applicazioni dell'utente corrente.

Si noti che i pacchetti di installazione che usano la proprietà [**LIMITUI**](limitui.md) devono anche contenere [**ARPNOMODIFY**](arpnomodify.md). Questa operazione è necessaria affinché un utente ottenga il comportamento corretto da installazione applicazioni nell'utilità pannello di controllo durante il tentativo di configurazione di un prodotto.

Il programma di installazione usa le seguenti [proprietà pubbliche](public-properties.md) per gestire installazione applicazioni nel pannello di controllo.

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
<td>URL del canale di aggiornamento per l'applicazione. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></td>
<td>Fornisce commenti per installazione applicazioni nel pannello di controllo. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></td>
<td>Fornisce il contatto per installazione applicazioni nel pannello di controllo. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></td>
<td>Percorso completo della cartella principale dell'applicazione. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></td>
<td>Indirizzo Internet, o URL, per il supporto tecnico. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></td>
<td>Numeri di telefono del supporto tecnico. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></td>
<td>Impedisce la visualizzazione di un pulsante modifica per il prodotto in Installazione applicazioni nel pannello di controllo.
<blockquote>
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP. Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></td>
<td>Impedisce la visualizzazione di un pulsante Rimuovi per il prodotto in Installazione applicazioni nel pannello di controllo. Il prodotto può comunque essere rimosso selezionando il pulsante modifica se il pacchetto di installazione è stato creato con un'interfaccia utente che fornisce la rimozione del prodotto come opzione.
<blockquote>
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP. Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></td>
<td>Disabilita il pulsante Ripristina di installazione applicazioni nel pannello di controllo.
<blockquote>
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP. Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></td>
<td>Identifica l'icona visualizzata in Installazione applicazioni. Se questa proprietà non è definita, Aggiungi/Rimuovi programmi specifica l'icona di visualizzazione.</td>
</tr>
<tr class="odd">
<td><a href="arpreadme.md"><strong>ARPREADME</strong></a></td>
<td>Include il file Leggimi per installazione applicazioni nel pannello di controllo. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="even">
<td><a href="arpsize.md"><strong>ARPSIZE</strong></a></td>
<td>Dimensioni stimate dell'applicazione in KB.</td>
</tr>
<tr class="odd">
<td><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></td>
<td>Impedisce la visualizzazione dell'applicazione nell'elenco programmi di installazione applicazioni nel pannello di controllo.
<blockquote>
<b>Nota:</b> Questa operazione influisca solo sulla visualizzazione in ARP. Il Windows Installer è ancora in grado di ripristinare, installare su richiesta e disinstallare le applicazioni tramite una riga di comando o l'interfaccia di programmazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></td>
<td>URL per la home page dell'applicazione. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
<tr class="odd">
<td><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></td>
<td>URL per le informazioni di aggiornamento dell'applicazione. Valore scritto dal programma di installazione sotto la <a href="uninstall-registry-key.md">chiave Disinstalla registro di sistema</a>.</td>
</tr>
</tbody>
</table>

> [!Note]  
> Per informazioni sullo strumento set Program and Defaults, vedere la sezione Utilizzo di [set Program Access e computer defaults](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disinstalla chiave del registro di sistema](uninstall-registry-key.md)
</dt> </dl>
