---
title: Informazioni sull'aggiornamento della piattaforma per Windows Vista
description: Viene fornita una panoramica sull'aggiornamento della piattaforma per Windows Vista e sull'aggiornamento della piattaforma per Windows Server 2008 e sulle relative funzionalità.
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Aggiornamento della piattaforma per Windows Server 2008
- Aggiornamento della piattaforma per Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321128"
---
# <a name="about-platform-update-for-windows-vista"></a>Informazioni sull'aggiornamento della piattaforma per Windows Vista

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono aggiornamenti del sistema operativo degli utenti finali che supportano l'utilizzo di tecnologie Windows 7 selezionate nelle versioni precedenti del sistema operativo Windows. Gli aggiornamenti includono un set di librerie di runtime che consentono agli sviluppatori di applicazioni di avere come destinazione le versioni correnti, Windows 7 e Windows Server 2008 R2, nonché le versioni precedenti, Windows Vista e Windows Server 2008.

## <a name="summary-of-supported-api-by-technology"></a>Riepilogo dell'API supportata per tecnologia

Ogni tecnologia supportata dall'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per gli aggiornamenti di Windows Server 2008 include un set di API che è possibile usare in un'applicazione destinata a una versione precedente di Windows.

Per ulteriori informazioni sull'utilizzo delle API supportate dagli aggiornamenti in un'applicazione destinata a versioni precedenti di Windows, vedere [sviluppo di applicazioni per versioni precedenti di Windows](developing-applications-for-previous-versions-of-windows.md).

> [!Note]  
> Alcune API associate a una tecnologia potrebbero non essere supportate e il comportamento, le prestazioni o i requisiti per alcune API supportate possono variare nelle diverse versioni di Windows. Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a>Tecnologie supportate con l'aggiornamento della piattaforma per Windows Vista

Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

Nella tabella seguente sono illustrate le tecnologie supportate per Windows Vista e Windows XP con l'aggiornamento della piattaforma per Windows Vista.

| Tecnologia                                                                                    | Windows Vista | Windows XP |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [API di automazione di Windows](#windows-automation-api)                                             | Sì           | Sì        |
| [Grafica di Windows, creazione di immagini e libreria XPS](#windows-graphics-imaging-and-xps-library)        | Sì           | No         |
| [Libreria della barra multifunzione di Windows e gestione animazioni](#windows-ribbon-and-animation-manager-library) | Sì           | No         |
| [Piattaforma per dispositivi portatili Windows](#windows-portable-devices-platform)                       | Sì           | No         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a>Tecnologie supportate con l'aggiornamento della piattaforma per Windows Server 2008

Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

Nella tabella seguente sono illustrate le tecnologie supportate per Windows Server 2008 e Windows Server 2003 con l'aggiornamento della piattaforma per Windows Server 2008.

| Tecnologia                                                                                    | Windows Server 2008 | Windows Server 2003 |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [API di automazione di Windows](#windows-automation-api)                                             | Sì                 | Sì                 |
| [Grafica di Windows, creazione di immagini e libreria XPS](#windows-graphics-imaging-and-xps-library)        | Sì                 | No                  |
| [Libreria della barra multifunzione di Windows e gestione animazioni](#windows-ribbon-and-animation-manager-library) | Sì                 | No                  |
| [Piattaforma per dispositivi portatili Windows](#windows-portable-devices-platform)                       | No                  | No                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a>Descrizioni dell'API supportata per tecnologia

Per informazioni dettagliate sull'API supportata per una tecnologia specifica, fare clic sul collegamento in una delle tabelle di riepilogo per passare alla sezione relativa a tale tecnologia.

-   [API di automazione di Windows](#windows-automation-api)
-   [Grafica di Windows, creazione di immagini e libreria XPS](#windows-graphics-imaging-and-xps-library)
-   [Libreria della barra multifunzione di Windows e gestione animazioni](#windows-ribbon-and-animation-manager-library)
-   [Piattaforma per dispositivi portatili Windows](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a>API di automazione di Windows

L'API di automazione di Windows 3,0 è un set di dll e di elementi API che consentono ai prodotti di Assistive Technology (AT) di offrire un migliore accesso ai computer per singoli utenti che hanno difficoltà fisiche o cognitive, problemi o disabilità. Inoltre, poiché l'API di automazione di Windows 3,0 consente alle applicazioni di accedere e modificare gli elementi dell'interfaccia utente di altre applicazioni, è una tecnologia ideale per l'implementazione di strumenti di test automatizzati.

Microsoft Active Accessibility (MSAA) e l'automazione dell'interfaccia utente sono simili in quanto entrambi forniscono un mezzo per esporre e raccogliere informazioni sugli elementi e i controlli dell'interfaccia utente per supportare l'accessibilità dell'interfaccia utente e l'automazione dei test software. Automazione interfaccia utente è un'implementazione di Windows della specifica di automazione interfaccia utente. Si tratta di una tecnologia più recente che risolve molte delle limitazioni di MSAA.

Per ulteriori informazioni sull'API di automazione di Windows 3,0, vedere [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 supportano la seguente API di automazione Windows 3,0:

-   [Microsoft Active Accessibility (MSAA)](#microsoft-active-accessibility-msaa)
-   [Automazione interfaccia utente](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a>Edizioni di Windows idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto per l'API di automazione di Windows 3,0 nelle edizioni di Windows illustrate nella tabella seguente.



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
<td><dl> Windows XP Home con SP3 (x86)<br />
Windows XP Professional con SP3 (x86)<br />
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

Microsoft Active Accessibility (MSAA) è una tecnologia legacy introdotta per la prima volta con Windows 95. Si tratta di un set di API che consente di migliorare il funzionamento dei prodotti Assistive Technology (AT) con le applicazioni eseguite in Microsoft Windows. L'API fornisce interfacce di programmazione e metodi per esporre le informazioni sugli elementi dell'interfaccia utente.

Per ulteriori informazioni su Microsoft Active Accessibility, vedere la [Panoramica tecnica](/windows/desktop/WinAuto/technical-overview).

### <a name="supported-microsoft-active-accessibility-api-elements"></a>Elementi API Microsoft Active Accessibility supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="ui-automation"></a>Automazione interfaccia utente

Automazione interfaccia utente è una tecnologia più recente che implementa la specifica di automazione interfaccia utente e risolve molte delle limitazioni di Microsoft Active Accessibility. Si tratta di un set di API che fornisce l'accesso programmatico agli elementi dell'interfaccia utente delle applicazioni. L'API fornita consente ai prodotti di Assistive Technology e agli strumenti di test automatici di accedere, identificare e modificare gli elementi dell'interfaccia utente standard e personalizzati di un'applicazione.

Per altre informazioni sull'automazione dell'interfaccia utente, vedere [API di automazione di Windows: automazione interfaccia utente](../winauto/entry-uiauto-win32.md).

### <a name="supported-ui-automation-api-elements"></a>Elementi API di automazione interfaccia utente supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="running-ui-automation-on-previous-windows-versions"></a>Esecuzione di automazione interfaccia utente nelle versioni precedenti di Windows

A causa delle differenze nel modo in cui i controlli comuni e i controlli standard di Windows sono implementati in versioni diverse di Windows, è possibile che si verifichino lievi differenze nelle informazioni che i proxy di automazione interfaccia utente recuperano per questi controlli da una versione a un'altra.

### <a name="windows-graphics-imaging-and-xps-library"></a>Grafica di Windows, creazione di immagini e libreria XPS

L'aggiornamento della piattaforma per Windows Vista supporta le seguenti API di Windows 7 dalla libreria grafica, imaging e XPS di Windows:

-   [Direct2D](#direct2d)
-   [Direct3D](#direct3d)
-   [DirectWrite](#directwrite)
-   [Packaging](#packaging)
-   [Componente Windows Imaging](#windows-imaging-component)
-   [Documento XPS](#xps-document)
-   [Stampa XPS](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a>Edizioni di Windows idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto della libreria XPS, della grafica e della creazione di immagini di Windows nelle edizioni di Windows illustrate nella tabella seguente.



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

L'API Direct2D è una nuova API grafica 2D in modalità immediata e con accelerazione hardware che fornisce prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo. L'API Direct2D è progettata per interagire correttamente con il codice esistente che usa GDI, GDI+ o Direct3D.

Per ulteriori informazioni su Direct2D, vedere [informazioni su Direct2D](/windows/desktop/Direct2D/direct2d-overview).

### <a name="supported-direct2d-api-elements"></a>Elementi API Direct2D supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="running-direct2d-on-previous-windows-versions"></a>Esecuzione di Direct2D nelle versioni precedenti di Windows

Se il driver WDDM 1,1 non è presente in Windows Vista, le prestazioni dell'interoperabilità Direct2D/GDI peggiorano.

### <a name="direct3d"></a>Direct3D

L'aggiornamento della piattaforma per Windows Vista fornisce il supporto di BGRA Surface per i percorsi di codice Direct3D10 e Direct3D 10.1. Direct3D10Level9 consente la funzionalità di Direct3D10 per l'uso di hardware Direct3D9. Direct3D WARP10 è un'applicazione di rasterizzazione software a prestazioni elevate per le applicazioni Direct3D10. Direct3D11, la versione più recente di Direct3D, fornisce nuove funzionalità, ad esempio il supporto per il multithreading migliorato, il mosaico, la funzionalità DirectCompute e il collegamento dinamico dello shader.

Se si creano applicazioni che usano Direct3D, [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) è obbligatorio).

Per ulteriori informazioni su Direct3D, vedere [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/default.aspx) .

### <a name="supported-direct3d-api-elements"></a>Elementi API Direct3D supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="directwrite"></a>DirectWrite

L'API DirectWrite è una nuova API di testo che offre più livelli di funzionalità, tra cui il layout del testo, l'elaborazione di script, il rendering del glifo e il sistema di tipi di carattere. DirectWrite usa i tipi di carattere OpenType e il rendering ClearType in pixel per migliorare l'esperienza di testo fornita dalle applicazioni. Il rendering del testo viene accelerato dall'hardware se usato con Direct2D.

Per ulteriori informazioni su DirectWrite, vedere [Introduzione a DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).

### <a name="supported-directwrite-api-elements"></a>Elementi API DirectWrite supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="running-directwrite-on-previous-windows-versions"></a>Esecuzione di DirectWrite nelle versioni precedenti di Windows

I problemi di comportamento seguenti potrebbero influire sull'uso dell'API DirectWrite nelle versioni precedenti di Windows:

-   Gli script nuovi in Windows 7 potrebbero non essere visualizzati correttamente nelle versioni precedenti di Windows.
-   Le impostazioni locali non disponibili nelle versioni precedenti di Windows eseguono il fallback al comportamento predefinito.
-   Il sintonizzatore ClearType non è disponibile nelle versioni precedenti di Windows.
-   L'interoperabilità GDI ha un costo di memoria superiore in alcuni scenari nelle versioni precedenti di Windows.

### <a name="packaging"></a>Packaging

L'aggiornamento della piattaforma per Windows Vista supporta un subset limitato di API per la creazione di pacchetti necessari per eseguire attività con l'API documenti XPS nelle applicazioni non gestite.

Per altre informazioni sulle API per la creazione di pacchetti, vedere [Panoramica dell'API](/previous-versions/windows/desktop/opc/packaging-api-overview)di creazione pacchetti.

### <a name="supported-packaging-api-elements"></a>Elementi API di creazione pacchetti supportati

Sono supportate solo le seguenti interfacce di creazione pacchetti:

-   IOpcUri
-   IOpcPartUri
-   IOpcFactory (sono supportati solo i metodi seguenti)
    -   CreatePackageRootUri
    -   CreatePartUri
    -   CreateStreamOnFile

Le API di creazione pacchetti supportate possono essere usate per creare flussi su file, nonché per creare e interagire con l'URI basato su pacchetti.

### <a name="running-packaging-api-on-previous-windows-versions"></a>Esecuzione dell'API di creazione pacchetti nelle versioni precedenti di Windows

Il comportamento e le prestazioni delle interfacce e dei metodi di creazione di pacchetti supportati sono gli stessi in tutte le piattaforme supportate.

Se un'applicazione tenta di creare un'istanza o chiamare un'interfaccia o un metodo di creazione pacchetto non supportato, il tentativo avrà esito negativo. Se la chiamata è a un metodo [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) non supportato, \_ viene restituito il codice di errore E NOTIMPL.

### <a name="windows-imaging-component"></a>Componente Windows Imaging

Le nuove funzionalità di Windows Imaging Component (WIC) includono una sicurezza avanzata, il supporto per l'interoperabilità con un colore elevato e una migliore interoperabilità dei metadati. Inoltre, il componente Windows Imaging amplia la conformità agli standard fornendo supporto per la decodifica progressiva delle immagini, le funzionalità PNG espanse, i metadati GIF, gli aggiornamenti delle foto HD e i metadati che si estendono sui segmenti APPn.

Per ulteriori informazioni sul componente Windows Imaging, vedere [Cenni preliminari sul componente Windows Imaging](/windows/desktop/wic/-wic-about-windows-imaging-codec).

### <a name="supported-wic-api-elements"></a>Elementi API WIC supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="xps-document"></a>Documento XPS

Le API documento XPS supportano la creazione, la modifica e il salvataggio di documenti XPS in applicazioni non gestite

Per ulteriori informazioni sulle API per documenti XPS, vedere la [Guida alla programmazione dei documenti XPS.](/previous-versions//dd372978(v=vs.85))

### <a name="supported-xps-document-api-elements"></a>Elementi API Document XPS supportati

Solo le interfacce delle [firme digitali XPS](/previous-versions/windows/desktop/dd372947(v=vs.85)) non sono supportate nelle versioni del sistema operativo di livello inferiore.

### <a name="xps-print"></a>Stampa XPS

Le API di stampa XPS supportano la stampa di documenti XPS da applicazioni basate su Windows.

Per altre informazioni sulle API di stampa XPS, vedere l' [API XpsPrint](/windows/desktop/printdocs/xpsprint-api).

### <a name="supported-xps-print-api-elements"></a>Elementi API di stampa XPS supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="windows-ribbon-and-animation-manager-library"></a>Libreria della barra multifunzione di Windows e gestione animazioni

L'aggiornamento della piattaforma per Windows Vista supporta le seguenti API di Windows 7 dalla barra multifunzione di Windows e dalla libreria di animazioni:

-   [Framework della barra multifunzione di Windows](#windows-ribbon-and-animation-manager-library)
-   [Gestione animazioni Windows](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a>Edizioni di Windows idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto della libreria della barra multifunzione di Windows e di gestione animazioni nelle edizioni di Windows illustrate nella tabella seguente.



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



 

### <a name="windows-ribbon-framework"></a>Framework della barra multifunzione di Windows

Il Framework della barra multifunzione di Windows è un sistema avanzato per la presentazione di comandi che offre un'alternativa moderna ai menu a più livelli, alle barre degli strumenti e ai riquadri delle attività delle applicazioni Windows tradizionali.

Il Framework è una raccolta di API Microsoft Win32 che forniscono una serie di nuove funzionalità dell'interfaccia utente per gli sviluppatori Windows e includono sia la barra multifunzione che un sistema di menu di scelta rapida.

Per ulteriori informazioni sul Framework della barra multifunzione, vedere [Introduzione al framework della barra](../windowsribbon/windowsribbon-introduction.md)multifunzione di Windows.

### <a name="supported-ribbon-framework-api-elements"></a>Elementi API Framework della barra multifunzione supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="windows-animation-manager"></a>Gestione animazioni Windows

Gestione animazioni Windows (animazione Windows) è un'interfaccia a livello di codice che supporta l'animazione di elementi visivi delle applicazioni Windows. L'animazione Windows è progettata per semplificare lo sviluppo e la gestione delle sequenze di animazione e consentire agli sviluppatori di implementare animazioni coerenti e intuitive. L'animazione Windows può essere usata con qualsiasi piattaforma grafica, ad esempio Direct2D, Direct3D o GDI+.

Animazione Windows è un'API COM a thread singolo che fornisce tutto ciò che uno sviluppatore deve creare, gestire e guidare l'animazione dell'interfaccia utente.

Per ulteriori informazioni su Windows Animation Manager, vedere [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).

### <a name="supported-animation-manager-api-elements"></a>Elementi API di gestione animazioni supportati

Tutte le API sono supportate nelle versioni precedenti di Windows che sono idonee per l'aggiornamento della piattaforma per Windows Vista o per l'aggiornamento della piattaforma per Windows Server 2008.

### <a name="windows-portable-devices-platform"></a>Piattaforma per dispositivi portatili Windows

L'aggiornamento della piattaforma per Windows Vista supporta le estensioni di Windows 7 per la piattaforma Windows Mobile Devices (WPD). Questa funzionalità consente ai computer di comunicare con i supporti e i dispositivi di archiviazione collegati. WPD offre una soluzione flessibile e affidabile per la comunicazione dei computer con fotocamere digitali, lettori musicali, telefoni cellulari e molti altri tipi di dispositivi connessi.

Per ulteriori informazioni sui dispositivi portatili Windows, vedere [dispositivi portatili Windows](/windows-hardware/drivers/portable/) ( https://docs.microsoft.com/windows-hardware/drivers/portable/) .

### <a name="windows-editions-eligible-for-the-updates"></a>Edizioni di Windows idonee per gli aggiornamenti

L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 abilitano il supporto per dispositivi portatili Windows (WPD) nelle edizioni di Windows illustrate nella tabella seguente.



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



 

### <a name="supported-wpd-api-elements"></a>Elementi API WPD supportati

La tabella seguente identifica le funzionalità supportate per Windows 7, Windows Vista e Windows Vista con aggiornamento della piattaforma per le versioni di Windows Vista del sistema operativo Windows.

| Funzionalità WPD                    | Windows 7 | Windows Vista | Windows Vista con aggiornamento della piattaforma per Windows Vista |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| MTP su USB                   | Sì       | Sì           | Sì                                                  |
| MTP su IP                    | Sì       | Sì           | Sì                                                  |
| MTP su Bluetooth             | Sì       | No            | Sì                                                  |
| Servizi per dispositivi WPD e MTP    | Sì       | No            | Sì                                                  |
| Automazione WPD                 | Sì       | No            | No                                                   |
| Multifunzione/multitransport | Sì       | No            | No                                                   |
| Device Stage                   | Sì       | No            | No                                                   |
| Piattaforma di sincronizzazione dei dispositivi           | Sì       | No            | No                                                   |



 

Per le edizioni di Windows 7 e Windows Vista in cui non è installato Microsoft Windows Media Player per impostazione predefinita (le edizioni N e KN), è necessario installare [Windows Media Format 11 SDK]( ../audio-and-video.md) ( https://msdn.microsoft.com/windows/bb190326.aspx) per abilitare la funzionalità WPD. Per ulteriori informazioni, vedere l' [articolo della Knowledge base](https://support.microsoft.com/kb/953693) ( https://go.microsoft.com/fwlink/p/?linkid=158715) , originariamente pubblicato come risoluzione per Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-portal.md)
</dt> <dt>

**Cenni preliminari**
</dt> <dt>

[Informazioni sull'aggiornamento della piattaforma per Windows Vista](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[Articolo della Knowledge base sull'aggiornamento della piattaforma per Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 