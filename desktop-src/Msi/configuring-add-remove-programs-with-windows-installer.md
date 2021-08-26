---
description: È possibile fornire tutte le informazioni necessarie per configurare Installazione applicazioni in Pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto del programma di installazione Windows dell'applicazione.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configurazione di Installazione applicazioni con il programma Windows installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48ad8499d395ffc4a5aad5491883f9c3161b78a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465488"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>Configurazione di Installazione applicazioni con il programma Windows installazione

È possibile fornire tutte le informazioni necessarie per configurare Installazione applicazioni in Pannello di controllo impostando i valori di determinate proprietà del programma di installazione nel pacchetto del programma di installazione Windows dell'applicazione. L'impostazione di queste proprietà consente di scrivere automaticamente i valori corrispondenti nel Registro di sistema. Se il programma di installazione rileva che il prodotto è contrassegnato per la rimozione completa, le operazioni vengono aggiunte automaticamente allo script per rimuovere la cartella Installazione applicazioni nelle informazioni Pannello di controllo per il prodotto.

Se un'applicazione non è registrata, non è elencata in Installazione applicazioni in Pannello di controllo. Per altre informazioni, vedere [Aggiunta e rimozione di un'applicazione e Nessuna traccia nel Registro di sistema.](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)

Le applicazioni installate nel contesto [](installation-context.md) di installazione per utente vengono visualizzate in Installazione applicazioni dell'utente corrente. Le applicazioni installate nel contesto di installazione per computer vengono visualizzate in Installazione applicazioni di tutti gli utenti. Le applicazioni che non sono state installate per computer e sono state installate solo come applicazioni per utente per utenti diversi dall'utente corrente, non vengono visualizzate in Installazione applicazioni dell'utente corrente.

Si noti che i pacchetti di installazione che usano [**la proprietà LIMITUI**](limitui.md) devono contenere anche [**ARPNOMODIFY.**](arpnomodify.md) Questo è necessario per un utente per ottenere il comportamento corretto da Installazione applicazioni nell'utilità Pannello di controllo quando si tenta di configurare un prodotto.

Il programma di installazione usa [le proprietà pubbliche seguenti](public-properties.md) per gestire Installazione applicazioni in Pannello di controllo.


| Nome proprietà | Breve descrizione della proprietà | 
|---------------|-------------------------------|
| <a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a> | URL del canale di aggiornamento per l'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a> | Fornisce commenti per Installazione applicazioni nel Pannello di controllo. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arpcontact.md"><strong>ARPCONTACT</strong></a> | Fornisce il contatto per Installazione applicazioni nel Pannello di controllo. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a> | Percorso completo della cartella primaria dell'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arphelplink.md"><strong>ARPHELPLINK</strong></a> | Indirizzo Internet, o URL, per il supporto tecnico. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a> | Numeri di telefono del supporto tecnico. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a> | Impedisce la visualizzazione di un pulsante Cambia per il prodotto in Installazione applicazioni nel Pannello di controllo.<blockquote><b>Nota:</b> Questo influisce solo sulla visualizzazione nel punto di accesso. Il Windows è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.</blockquote><br /> | 
| <a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a> | Impedisce la visualizzazione di un pulsante Rimuovi per il prodotto in Installazione applicazioni nel Pannello di controllo. Il prodotto può comunque essere rimosso selezionando il pulsante Cambia se il pacchetto di installazione è stato creato con un'interfaccia utente che consente la rimozione del prodotto come opzione.<blockquote><b>Nota:</b> Questo influisce solo sulla visualizzazione nel punto di accesso. Il Windows è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.</blockquote><br /> | 
| <a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a> | Disabilita il pulsante Ripristina in Installazione applicazioni nel Pannello di controllo.<blockquote><b>Nota:</b> Questo influisce solo sulla visualizzazione nel punto di accesso. Il Windows è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.</blockquote><br /> | 
| <a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a> | Identifica l'icona visualizzata in Installazione applicazioni. Se questa proprietà non è definita, Installazione applicazioni specifica l'icona di visualizzazione. | 
| <a href="arpreadme.md"><strong>ARPREADME</strong></a> | Fornisce il file Leggimi per Installazione applicazioni in Pannello di controllo. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arpsize.md"><strong>ARPSIZE</strong></a> | Dimensioni stimate dell'applicazione in KB. | 
| <a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a> | Impedisce la visualizzazione dell'applicazione nell'elenco Programmi di Installazione applicazioni nel Pannello di controllo.<blockquote><b>Nota:</b> Questo influisce solo sulla visualizzazione nel punto di accesso. Il Windows è ancora in grado di ripristinare, installare e disinstallare applicazioni su richiesta tramite una riga di comando o l'interfaccia di programmazione.</blockquote><br /> | 
| <a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a> | URL per il nome dell'home page. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 
| <a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a> | URL per le informazioni sull'aggiornamento dell'applicazione. Valore scritto dal programma di installazione nella chiave <a href="uninstall-registry-key.md">del Registro di sistema Uninstall</a>. | 


> [!Note]  
> Per informazioni sullo strumento Imposta programmi e impostazioni predefinite, vedere la sezione [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Disinstallare la chiave del Registro di sistema](uninstall-registry-key.md)
</dt> </dl>
