---
title: Informazioni sull'aggiornamento della piattaforma Windows Vista
description: Offre una panoramica dell'aggiornamento della piattaforma per Windows Vista e dell'aggiornamento della piattaforma per Windows Server 2008 e delle relative funzionalità.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Aggiornamento della piattaforma per Windows Server 2008
- Aggiornamento della piattaforma per Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9751331bf764ee486afe20a9dccd7f6b4691fee15e5000ccf8157561656409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964570"
---
# <a name="about-platform-update-for-windows-vista"></a>Informazioni sull'aggiornamento della piattaforma Windows Vista

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono aggiornamenti del sistema operativo dell'utente finale che supportano l'uso di tecnologie Windows 7 selezionate nelle versioni precedenti del sistema operativo Windows. Gli aggiornamenti includono un set di librerie di runtime che consentono agli sviluppatori di applicazioni di scegliere come destinazione le versioni correnti, Windows 7 e Windows Server 2008 R2, nonché le versioni precedenti, Windows Vista e Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Riepilogo dell'API supportata in base alla tecnologia

Ogni tecnologia supportata dall'aggiornamento della piattaforma per Windows Vista e dall'aggiornamento della piattaforma per gli aggiornamenti di Windows Server 2008 include un set di API che può essere usato in un'applicazione destinata alla versione precedente di Windows.

Per altre informazioni sull'uso delle API supportate dagli aggiornamenti in un'applicazione destinata a versioni precedenti di Windows, vedere Sviluppo di applicazioni per le versioni precedenti [di Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Alcune API associate a una tecnologia potrebbero non essere supportate e il comportamento, le prestazioni o i requisiti per alcune API supportate possono variare a seconda Windows versioni. Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Tecnologie supportate con l'aggiornamento della piattaforma per Windows Vista

Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

Le tecnologie supportate per Windows Vista e Windows XP con l'aggiornamento della piattaforma per Windows Vista sono illustrate nella tabella seguente.

| Tecnologia                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [API di automazione di Windows](#windows-automation-api)                                             | Sì           | Sì        |
| [Windows Grafica, creazione di immagini e libreria XPS](#windows-graphics-imaging-and-xps-library)        | Sì           | No         |
| [Windows Libreria di Gestione animazioni e della barra multifunzione](#windows-ribbon-and-animation-manager-library) | Sì           | No         |
| [Windows Piattaforma per dispositivi portatili](#windows-portable-devices-platform)                       | Sì           | No         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Tecnologie supportate con l'aggiornamento della piattaforma Windows Server 2008

Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

Nella tabella seguente sono illustrate le tecnologie supportate per Windows Server 2008 e Windows Server 2003 con l'aggiornamento della piattaforma per Windows Server 2008.

| Tecnologia                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [API di automazione di Windows](#windows-automation-api)                                             | Sì                 | Sì                 |
| [Windows Grafica, creazione di immagini e libreria XPS](#windows-graphics-imaging-and-xps-library)        | Sì                 | No                  |
| [Windows Libreria di Gestione animazioni e della barra multifunzione](#windows-ribbon-and-animation-manager-library) | Sì                 | No                  |
| [Windows Piattaforma per dispositivi portatili](#windows-portable-devices-platform)                       | No                  | No                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descrizioni dell'API supportata dalla tecnologia

Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

-   [API di automazione di Windows](#windows-automation-api)
-   [Windows Grafica, creazione di immagini e libreria XPS](#windows-graphics-imaging-and-xps-library)
-   [Windows Libreria di Gestione animazioni e della barra multifunzione](#windows-ribbon-and-animation-manager-library)
-   [Windows Piattaforma per dispositivi portatili](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>API di automazione di Windows

Windows L'API di automazione 3.0 è un set di DLL ed elementi API che consentono ai prodotti Assistive Technology (AT) di fornire un migliore accesso ai computer per gli utenti con problemi fisici o cognitivi, problemi o disabilità. Inoltre, poiché l Windows API di Automazione 3.0 consente alle applicazioni di accedere e modificare gli elementi dell'interfaccia utente di altre applicazioni, è una tecnologia ideale per l'implementazione di strumenti di test automatizzati.

Microsoft Active Accessibility (MSAA) e Automazione interfaccia utente sono simili in quanto entrambi consentono di esporre e raccogliere informazioni sugli elementi e sui controlli dell'interfaccia utente per supportare l'accessibilità dell'interfaccia utente e l'automazione dei test software. Automazione interfaccia utente è un'implementazione Windows della specifica Automazione interfaccia utente. Si tratta di una tecnologia più recente che risolve molte delle limitazioni di MSAA.

Per altre informazioni sull'API Windows Automation 3.0, vedere API [Windows Automation: Panoramica.](/windows/desktop/WinAuto/windows-automation-api-overview)

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 supportano l'API Windows Automation 3.0 seguente:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Automazione interfaccia utente](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edizioni idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto dell'API di automazione di Windows 3.0 nelle edizioni di Windows illustrate nella tabella seguente.



<table>
<thead>
<tr class="header">
<th>Versione di Windows</th>
<th>Edizioni idonee per l'aggiornamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 e amd64)<br />
Home Premium con SP2 (x86 e amd64)<br />
Business con SP2 (x86 e amd64)<br />
Enterprise con SP2 (x86 e amd64)<br />
Ultimate con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows XP</td>
<td><dl> Windows XP Home with SP3 (x86)<br />
Windows Xp Professional con SP3 (x86)<br />
</dl></td>
</tr>
<tr class="odd">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2003</td>
<td><dl> Windows Server 2003 con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a>Microsoft Active Accessibility (MSAA)

Microsoft Active Accessibility (MSAA) è una tecnologia legacy introdotta per la prima volta con Windows 95. Si tratta di un set di API che migliora il modo in cui i prodotti Assistive Technology (AT) funzionano con le applicazioni in esecuzione in Microsoft Windows. L'API fornisce interfacce di programmazione e metodi per esporre informazioni sugli elementi dell'interfaccia utente.

Per altre informazioni sui Microsoft Active Accessibility, vedere [Panoramica tecnica](/windows/desktop/WinAuto/technical-overview)di .

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Elementi api Microsoft Active Accessibility supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="ui-automation"></a>Automazione interfaccia utente

Automazione interfaccia utente è una tecnologia più recente che implementa la specifica Automazione interfaccia utente e risolve molte delle limitazioni di Microsoft Active Accessibility. Si tratta di un set di API che fornisce l'accesso a livello di codice agli elementi dell'interfaccia utente delle applicazioni. L'API fornita consente ai prodotti Assistive Technology e agli strumenti di test automatizzati di accedere, identificare e modificare gli elementi standard e personalizzati dell'interfaccia utente di un'applicazione.

Per altre informazioni sui Automazione interfaccia utente, vedere [API Windows Automation: Automazione interfaccia utente](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Elementi api Automazione interfaccia utente supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Esecuzione Automazione interfaccia utente nelle versioni Windows precedenti

A causa delle differenze nel modo in cui i controlli comuni e i controlli standard di Windows vengono implementati in diverse versioni di Windows, potrebbero esserci lievi differenze nelle informazioni recuperate dai proxy di Automazione interfaccia utente per questi controlli da una versione a un'altra.

### <a name="windows-graphics-imaging-and-xps-library"></a>Windows Grafica, creazione di immagini e libreria XPS

L'aggiornamento della piattaforma per Windows Vista supporta le seguenti API Windows 7 dalla libreria Windows Graphics, Imaging e XPS:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Packaging](#packaging)
-   [Componente Windows Imaging](#windows-imaging-component)
-   [Documento XPS](#xps-document)
-   [Stampa XPS](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edizioni idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto della grafica, dell'immagine e della libreria XPS di Windows nelle edizioni di Windows illustrate nella tabella seguente.



<table>
<thead>
<tr class="header">
<th>Versione di Windows</th>
<th>Edizioni idonee per l'aggiornamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 e amd64)<br />
Home Premium con SP2 (x86 e amd64)<br />
Business con SP2 (x86 e amd64)<br />
Enterprise con SP2 (x86 e amd64)<br />
Ultimate con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a>Direct2D

L'API Direct2D è una nuova API grafica 2D in modalità immediata con accelerazione hardware che offre prestazioni elevate e rendering di alta qualità per geometria 2D, bitmap e testo. L'API Direct2D è progettata per interagire bene con il codice esistente che usa GDI, GDI+ o Direct3D.

Per altre informazioni su Direct2D, vedere [Informazioni su Direct2D.](/windows/desktop/Direct2D/direct2d-overview)

### <a name="supported-direct2d-api-elements"></a>Elementi API Direct2D supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>Esecuzione di Direct2D in versioni Windows precedenti

Se il driver WDDM 1.1 non è presente in Windows Vista, le prestazioni dell'interoperabilità Direct2D/GDI si riducono.

### <a name="direct3d"></a>Direct3D

L'aggiornamento della piattaforma Windows Vista offre il supporto della superficie BGRA per i percorsi di codice Direct3D10 e Direct3D10.1. Direct3D10Level9 abilita la funzionalità Direct3D10 per il funzionamento su hardware Direct3D9. Direct3D WARP10 è un rasterizzatore software a prestazioni performanti per le applicazioni Direct3D10. Direct3D11, la versione più recente di Direct3D, offre nuove funzionalità, ad esempio il supporto del multithreading migliorato, la funzionalità a tessellazione, la funzionalità DirectCompute e il collegamento dinamico dello shader.

Se si creano applicazioni che usano Direct3D, [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) è obbligatorio.

Per altre informazioni su Direct3D, vedere [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Elementi api Direct3D supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

L DirectWrite API è una nuova API di testo che offre più livelli di funzionalità, tra cui layout del testo, elaborazione di script, rendering del glifo e sistema di tipi di carattere. DirectWrite usa tipi di carattere OpenType e rendering ClearType sub-pixel per migliorare l'esperienza di testo fornita dalle applicazioni. Il rendering del testo è con accelerazione hardware quando viene usato con Direct2D.

Per altre informazioni sui DirectWrite, vedere [Introduzione DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Elementi api DirectWrite supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>Esecuzione DirectWrite nelle versioni Windows precedenti

I problemi di comportamento seguenti possono influire sull'uso dell'API DirectWrite nelle versioni Windows precedenti:

-   È possibile che il rendering degli script Windows 7 non venga eseguito correttamente nelle versioni Windows precedenti.
-   Le impostazioni locali non disponibili nelle versioni Windows precedenti e il comportamento predefinito.
-   Il siner ClearType non è disponibile nelle versioni Windows precedenti.
-   L'interoperabilità GDI ha un costo di memoria superiore in alcuni scenari nelle versioni Windows precedenti.

### <a name="packaging"></a>Packaging

L'aggiornamento della piattaforma per Windows Vista supporta un subset limitato delle API di creazione pacchetti necessarie per eseguire attività con l'API documento XPS nelle applicazioni non gestite.

Per altre informazioni sulle API per la creazione di pacchetti, vedere Panoramica [dell'API di creazione pacchetti.](/previous-versions/windows/desktop/opc/packaging-api-overview)

### <a name="supported-packaging-api-elements"></a>Elementi api di creazione pacchetti supportati

Sono supportate solo le interfacce di creazione pacchetti seguenti:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (sono supportati solo i metodi seguenti)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

Le API di creazione pacchetti supportate possono essere usate per creare flussi su file, nonché per creare e interagire con l'URI basato su pacchetto.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Esecuzione dell'API di creazione pacchetti nelle versioni Windows precedenti

Il comportamento e le prestazioni delle interfacce e dei metodi di creazione pacchetti supportati sono gli stessi in tutte le piattaforme supportate.

Se un'applicazione tenta di creare un'istanza o chiamare un'interfaccia o un metodo di creazione di pacchetti non supportato, il tentativo avrà esito negativo. Se la chiamata è a un metodo [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) non supportato, verrà restituito il codice di errore E \_ NOTIMPL.

### <a name="windows-imaging-component"></a>Componente Windows Imaging

Le nuove funzionalità del Windows Imaging Component (WIC) includono sicurezza avanzata, supporto per colori elevati e migliore interoperabilità dei metadati. Inoltre, il componente Windows Imaging amplia la conformità agli standard fornendo il supporto per la decodifica progressiva delle immagini, le funzionalità PNG espanse, i metadati GIF, , gli aggiornamenti delle foto HD e i metadati che si estendono sui segmenti APPn.

Per altre informazioni sul componente di Windows imaging, vedere cenni preliminari Windows del componente di creazione [dell'immagine.](/windows/desktop/wic/-wic-about-windows-imaging-codec)

### <a name="supported-wic-api-elements"></a>Elementi API WIC supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="xps-document"></a>Documento XPS

Le API documento XPS supportano la creazione, la modifica e il salvataggio di documenti XPS in applicazioni non gestite

Per altre informazioni sulle API documento XPS, vedere la Guida alla programmazione [di documenti XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Elementi DELL'API documento XPS supportati

Solo le interfacce delle firme digitali [XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) non sono supportate nelle versioni del sistema operativo di livello inferiore.

### <a name="xps-print"></a>Stampa XPS

Le API di stampa XPS supportano la stampa di documenti XPS Windows applicazioni basate su client.

Per altre informazioni sulle API di stampa XPS, vedere [l'API XpsPrint](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Elementi dell'API di stampa XPS supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Windows Libreria di Gestione animazioni e della barra multifunzione

L'aggiornamento della piattaforma Windows Vista supporta le SEGUENTI API Windows 7 dalla barra multifunzione Windows e Libreria animazioni:

-   [Windows Framework della barra multifunzione](#windows-ribbon-and-animation-manager-library)
-   [Windows Gestione animazione](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edizioni idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto della barra multifunzione Windows e della libreria di gestione animazione nelle edizioni di Windows illustrate nella tabella seguente.



<table>
<thead>
<tr class="header">
<th>Versione di Windows</th>
<th>Edizioni idonee per l'aggiornamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 e amd64)<br />
Home Premium con SP2 (x86 e amd64)<br />
Business con SP2 (x86 e amd64)<br />
Enterprise con SP2 (x86 e amd64)<br />
Ultimate con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
<tr class="even">
<td>Windows Server 2008</td>
<td><dl> Windows Server 2008 con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a>Windows Framework della barra multifunzione

Il framework Windows barra multifunzione è un sistema di presentazione dei comandi ricco che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri attività delle applicazioni Windows tradizionali.

Il framework è una raccolta di API Win32 Microsoft che forniscono una serie di nuove funzionalità dell'interfaccia utente per gli sviluppatori Windows e include sia la barra multifunzione che un sistema di menu di scelta rapida.

Per altre informazioni sul framework della barra multifunzione, vedere [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).

### <a name="supported-ribbon-framework-api-elements"></a>Elementi API del framework della barra multifunzione supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="windows-animation-manager"></a>Windows Gestione animazioni

Windows Animation Manager (Windows Animation) è un'interfaccia a livello di codice che supporta l'animazione di elementi visivi di Windows applicazioni. Windows L'animazione è progettata per semplificare lo sviluppo e la manutenzione delle sequenze di animazione e per consentire agli sviluppatori di implementare animazioni coerenti e intuitive. Windows L'animazione può essere usata con qualsiasi piattaforma grafica, tra cui Direct2D, Direct3D o GDI+.

Windows L'animazione è un'API COM a thread singolo che fornisce tutto ciò che uno sviluppatore deve creare, gestire e guidare l'animazione dell'interfaccia utente.

Per altre informazioni su Gestione Windows animazione, vedere [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Elementi API di Gestione animazioni supportati

Tutte le API sono supportate nelle versioni precedenti di Windows idonee per l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Windows Piattaforma per dispositivi portatili

L'aggiornamento della piattaforma Windows Vista supporta Windows 7 estensioni per la piattaforma Windows WPD (Portable Devices). Questa funzionalità consente ai computer di comunicare con i supporti collegati e i dispositivi di archiviazione. La piattaforma WPD offre un modo flessibile e affidabile per comunicare con fotocamere digitali, lettori musicali, telefoni cellulari e molti altri tipi di dispositivi connessi.

Per altre informazioni sui Windows portatili, vedere Windows [dispositivi portatili](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Windows Edizioni idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto di Windows Portable Devices (WPD) nelle edizioni di Windows illustrate nella tabella seguente.



<table>
<thead>
<tr class="header">
<th>Versione di Windows</th>
<th>Edizioni idonee per l'aggiornamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><dl> Starter con SP2 (x86)<br />
Home Basic con SP2 (x86 e amd64)<br />
Home Premium con SP2 (x86 e amd64)<br />
Business con SP2 (x86 e amd64)<br />
Enterprise con SP2 (x86 e amd64)<br />
Ultimate con SP2 (x86 e amd64)<br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a>Elementi api WPD supportati

La tabella seguente identifica le funzionalità supportate per le versioni Windows 7, Windows Vista e Windows Vista con Aggiornamento piattaforma per Windows Vista del sistema operativo Windows.

| Funzionalità WPD                    | Windows 7 | Windows Vista | Windows Vista con l'aggiornamento della piattaforma per Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP su USB                   | Sì       | Sì           | Sì                                                  |
| MTP su IP                    | Sì       | Sì           | Sì                                                  |
| MTP su Bluetooth             | Sì       | No            | Sì                                                  |
| Servizi dispositivi WPD e MTP    | Sì       | No            | Sì                                                  |
| Automazione WPD                 | Sì       | No            | No                                                   |
| Multi-funzione/multitrasporto | Sì       | No            | No                                                   |
| Device Stage                   | Sì       | No            | No                                                   |
| Piattaforma di sincronizzazione dei dispositivi           | Sì       | No            | No                                                   |



 

Per le edizioni di Windows 7 e Windows Vista in cui microsoft Windows Media Player non è installato per impostazione predefinita (le edizioni N e KN), è necessario installare [Windows Media Format 11 SDK]( ../audio-and-video.md) ( per abilitare la funzionalità https://msdn.microsoft.com/windows/bb190326.aspx) WPD. Per altre informazioni, vedere [l'articolo Knowledge Base](https://support.microsoft.com/kb/953693) ( , originariamente pubblicato come risoluzione https://go.microsoft.com/fwlink/p/?linkid=158715) per Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Cenni preliminari**
</dt> <dt>

[Informazioni sull'aggiornamento della piattaforma Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Knowledge Base articolo sull'aggiornamento della piattaforma per Windows Vista (kb 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 