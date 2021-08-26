---
description: Windows Acquisizione di immagini (WIA) è la piattaforma di acquisizione di immagini fisse nella famiglia di sistemi operativi Windows a partire da Windows Millennium Edition (Windows Me) e Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: Acquisizione di immagini di Windows (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e467d76f054a8cccb4c309f69b211d0d3d6fbe949625324c871319028aa78ebc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057011"
---
# <a name="windows-image-acquisition-wia"></a>Acquisizione di immagini di Windows (WIA)

Windows Acquisizione di immagini (WIA) è la piattaforma di acquisizione di immagini fisse nella famiglia di sistemi operativi Windows a partire da Windows Millennium Edition (Windows Me) e Windows XP.

-   [Introduzione](#introduction)
-   [Vantaggi dell Windows'acquisizione di immagini 2.0](#benefits-of-windows-image-acquisition-20)
    -   [Per i writer di applicazioni](#for-application-writers)
    -   [Per produttori di dispositivi](#for-device-manufactures)
    -   [Per gli utenti dello scanner](#for-scanner-users)
-   [Sviluppo di Windows di immagini](#development-of-windows-image-acquisition)
-   [Panoramica dell'Windows di immagini](#overview-of-windows-image-acquisition)
-   [Informazioni su Windows Image Acquisition 2.0](#facts-about-windows-image-acquisition-20)
-   [Destinatari degli sviluppatori](#developer-audience)
-   [Requisiti di run-time](#run-time-requirements)
-   [Argomenti relativi a WIA](#wia-topics)

## <a name="introduction"></a>Introduzione

La piattaforma WIA consente alle applicazioni di creazione di immagini/grafica di interagire con l'hardware di creazione delle immagini e standardizza l'interazione tra applicazioni e scanner diversi. In questo modo, le diverse applicazioni possono interagire con tali scanner e interagire con tali scanner senza richiedere agli autori e ai produttori di applicazioni di personalizzare l'applicazione o i driver per ogni combinazione applicazione-dispositivo.

![immagine che illustra l'architettura di base di wia come livello bidiredireale tra applicazioni e dispositivi di creazione di immagini. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Vantaggi dell Windows'acquisizione di immagini 2.0

WIA offre vantaggi agli sviluppatori di applicazioni, ai produttori di dispositivi e agli utenti dello scanner che devono interagire con l'hardware di creazione dell'immagine.

### <a name="for-application-writers"></a>Per i writer di applicazioni

-   Windows un processo di certificazione per i driver WIA in modo che le applicazioni WIA siano compatibili a livello di base con tutti gli scanner basati su WIA.
-   I driver WIA vengono caricati nel processo del servizio WIA, offrendo così un ambiente driver più stabile.
-   Le applicazioni possono essere avviate dal pulsante di analisi dello scanner tramite eventi push supportati dal sottosistema WIA.
-   WiA include un filtro di segmentazione predefinito che tutti i driver possono sfruttare. In questo modo, le applicazioni non devono scrivere codice per l'analisi in più aree per scopi quali la separazione di un numero elevato di foto distribuite su uno scanner a letti flat.

### <a name="for-device-manufactures"></a>Per produttori di dispositivi

-   Il processo di certificazione dei driver WIA consente agli sviluppatori di driver di stabilire che il driver è conforme a WIA.
-   I driver WIA possono sfruttare un filtro di segmentazione predefinito, un filtro di elaborazione delle immagini e un gestore degli errori, se scelgono di farlo.
-   Gli scanner basati su WIA funzionano Windows con applicazioni di analisi Windows come Windows Fax e Scan e Paint.
-   I driver WIA offrono una migliore integrazione con Windows, ad esempio l'esperienza completa del dispositivo.
-   Windows La versione di Vista include un driver di classe WSD-WIA che consente a tutti i dispositivi conformi al protocollo WS-Scan (Web Services for Scanner) di funzionare con applicazioni WIA senza driver o software aggiuntivi.

### <a name="for-scanner-users"></a>Per gli utenti dello scanner

-   Gli scanner basati su WIA possono essere usati da Windows applicazioni quali Windows Fax e Scansione e Paint senza la necessità di software aggiuntivo.
-   Le applicazioni e gli scanner basati su WIA possono anche sfruttare i componenti aggiuntivi WIA, ad esempio il filtro di segmentazione, che abilita funzionalità come l'elaborazione di un numero di immagini sullo scanner e la scansione di tutti i singoli file senza l'intervento dell'utente.
-   I dispositivi basati su WIA offrono un'integrazione molto migliore con altre Windows, ad esempio la funzionalità Device Stage per Windows 7.
-   WIA offre un'esperienza di analisi più affidabile, stabile e isolando il driver e l'applicazione.

## <a name="development-of-windows-image-acquisition"></a>Sviluppo di Windows di immagini

L'architettura di creazione dell'immagine in Windows 2000 e Windows 95 o versioni successive consisteva in un'astrazione hardware di basso livello, l'architettura di immagini statiche (STI) e un set di API di alto livello noto come TWAIN. In Windows è stato introdotto WINDOWS WINDOWS XP e Windows Me. WIA è un'architettura di creazione di immagini che si basa su STI e non richiede TWAIN, anche se TWAIN è ancora supportato insieme a WIA.

WIA 1.0 è stato introdotto in Windows Me e Windows XP e supporta scanner, fotocamere digitali e apparecchiature video digitali. WIA 2.0 è stato rilasciato con Windows Vista. WIA 2.0 è destinato agli scanner, ma continua a offrire supporto per applicazioni e dispositivi WIA 1.0 legacy tramite un livello di compatibilità da WIA 1.0 a WIA 2.0 fornito dal servizio WIA. Tuttavia, il supporto del contenuto video è stato rimosso da WIA per Windows Vista. È consigliabile Windows'API WPD (Portable Devices) per fotocamere digitali e apparecchiature video digitali in futuro. I driver WIA 1.0 e STI TWAIN sono ancora supportati direttamente in Windows Vista e Windows 7 insieme ai driver di dispositivo e alle applicazioni di creazione di immagini WIA 2.0 native.

## <a name="overview-of-windows-image-acquisition"></a>Panoramica dell'Windows di immagini

WIA offre un framework che consente a un dispositivo di presentare le proprie funzionalità univoche al sistema operativo e consente alle applicazioni di creazione di immagini di richiamare tali funzionalità univoche.

La piattaforma WIA include un protocollo di acquisizione dati, un modello e un'interfaccia DDI (Device Driver Model and Interface), un'API e un servizio WIA dedicato. La piattaforma include anche un set di driver in modalità kernel predefiniti che supportano la comunicazione con i dispositivi di creazione di immagini connessi localmente tramite interfacce USB, seriali/parallele, SCSI e FireWire. Il sottosistema WIA include anche un livello di compatibilità trasparente che consente alle applicazioni compatibili con TWAIN di usare e usare dispositivi basati su driver WIA.

I dispositivi di creazione di immagini connessi alla rete che supportano il protocollo WSD (Web Services for Devices) possono essere usati anche da applicazioni di creazione di immagini conformi a WIA in Windows Vista e Windows 7 tramite un driver di classe WSD-WIA fornito come parte di Windows Vista. Il driver di classe converte le chiamate WIA in chiamate WSD e viceversa e fa funzionare le applicazioni WIA già esistenti con scanner basati su WSD senza driver aggiuntivo.

I driver WIA sono formati da un componente dell'interfaccia utente e da un componente driver principale, caricati in due diversi spazi di processo: l'interfaccia utente nello spazio applicazione e il core del driver nello spazio dei servizi WIA. Il servizio viene eseguito nel contesto del sistema locale in Windows XP ed eseguito nel contesto del servizio locale a partire da Windows Server 2003 e Windows Vista per una sicurezza avanzata da driver dannosi o bug.

![immagine che illustra l'architettura di wia e il suo funzionamento come servizio.](images/wia-arch.png)

Il set di API WIA espone le applicazioni di creazione di immagini alla funzionalità hardware di acquisizione immagini fisse fornendo il supporto per:

-   Enumerazione dei dispositivi di acquisizione di immagini disponibili.
-   Creazione simultanea di connessioni a più dispositivi.
-   Esecuzione di query delle proprietà dei dispositivi in modo standard ed espandibile.
-   Acquisizione dei dati dei dispositivi tramite meccanismi di trasferimento standard e ad alte prestazioni.
-   Gestione delle proprietà dell'immagine tra trasferimenti di dati.
-   Notifica dello stato del dispositivo e della gestione degli eventi di analisi.

Windows aggiunto il supporto di scripting per WIA rilasciando la libreria di automazione WIA nel 2002 incorporata in Windows Vista come livello di automazione di acquisizione di immagini Windows (WIA) e continua a far parte di Windows 7. La libreria di automazione WIA offre funzionalità end-to-end di acquisizione di immagini agli ambienti di sviluppo di applicazioni abilitate per l'automazione e ai linguaggi di programmazione, ad esempio Microsoft Visual Basic 6.0, Active Server Pages (ASP), VBScript e \# C.

Per Windows 7, le API WIA hanno un supporto aggiuntivo per integrare il supporto per l'analisi push già esistente.

-   Analisi avviata dal dispositivo configurata automaticamente con parametri di analisi configurati nello scanner nel pannello anteriore del dispositivo.
-   Selezione automatica dell'origine per l'analisi avviata dal dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Informazioni su Windows Image Acquisition 2.0

-   Il meccanismo di trasferimento dei dati in WIA 2.0 è basato sul flusso. L'astrazione del flusso rimuove la distinzione tra tipi di trasferimento diversi e consente anche lo scambio di metadati reciprocamente concordati tra dispositivo e applicazione.
-   Il sottosistema WIA 2.0 include anche un componente aggiuntivo del driver di filtro di elaborazione immagini di base che può essere sostituito facoltativamente dal driver dello scanner, se il driver sceglie di fornire un filtro di elaborazione delle immagini personalizzato. Il filtro predefinito consente la post-elaborazione delle immagini acquisite tramite lo scanner. Il filtro di elaborazione delle immagini abilita anche le anteprime software in tempo reale quando vengono regolate impostazioni di piccole dimensioni, ad esempio luminosità e contrasto.
-   Il filtro di segmentazione è un altro pratico componente WIA che può essere sostituito da un filtro più personalizzato dal driver dello scanner. Il filtro di segmentazione può essere usato per l'analisi in più aree. L'analisi in più aree, ad esempio, consente a un'applicazione di rilevare automaticamente aree di analisi diverse senza alcun intervento da parte dell'utente, ad esempio identificando un gruppo di foto che si trova in modo casuale sul piano dello scanner.
-   WIA 2.0 fornisce un gestore degli errori sostituibile/estendibile per gestire correttamente ed eventualmente recuperare errori e ritardi di software, hardware e configurazione. Il gestore degli errori è un altro componente WIA che può essere sostituito con una versione più personalizzata dal driver dello scanner. Questa estensione fornisce messaggi di stato e di errore durante le acquisizioni dei dati, ad esempio "Lamp warming up", "Cover open", "Paper jam" e così via. Questa estensione consente anche un supporto più pulito per le operazioni di annullamento.

## <a name="developer-audience"></a>Sviluppatori

L'API WIA è progettata per l'uso da parte dei programmatori C/C++. È necessaria una familiarità con Windows gui e Component Object Model (COM).

Per gli sviluppatori che hanno familiarità con Microsoft Visual Basic 6.0, Active Server Pages (ASP) o scripting, WIA offre un livello di automazione per Windows XP Service Pack 1 (SP1) o versione successiva che si basa e semplifica l'accesso alle basi fornite da C/C++. Per informazioni sul livello di automazione, vedere Windows [Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> WiA Automation Layer sostituisce Windows di acquisizione di immagini (WIA) 1.0.

 

## <a name="run-time-requirements"></a>Requisiti di runtime

Le applicazioni che usano l'API WIA richiedono Windows XP o versioni successive.

## <a name="wia-topics"></a>Argomenti di WIA

Gli argomenti di WIA sono organizzati come illustrato nella tabella seguente.



|  Argomento                                                                                                                            | Descrizione                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Informazioni Windows'acquisizione di immagini](-wia-about-windows-image-acquisition.md)                                                  | Informazioni generali su WIA                                                                     |
| [Windows Driver di acquisizione immagini](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Sviluppo di driver WIA                                                                            |
| [Windows Livello di automazione acquisizione immagini](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Livello di automazione WIA                                                                              |
| [Esercitazione su WIA](-wia-wia-tutorial.md)                                                                                        | Procedura dettagliata del codice incluso nel Software Development Kit (SDK) in particolare per attività specifiche |
| [Riferimento](-wia-reference.md)                                                                                              | Informazioni su interfacce, metodi, oggetti e tipi di dati WIA usati in C/C++ e script.      |



 

 

 
