---
title: Panoramica di Biometric Framework
description: Il supporto nativo per i dispositivi biometrici è incorporato in Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a72b7bb6eab6a062b4dae51f729641607bcadc05dc7b0c50d12f6d59d729ae9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622701"
---
# <a name="biometric-framework-overview"></a>Panoramica di Biometric Framework

Ogni utente ha caratteristiche univoche che possono essere usate per l'identificazione. In genere queste caratteristiche sono fisiche e includono tratti come le impronte digitali, ma possono anche includere tratti comportamentali come andatura e ritmo di digitazione. Il termine biometria comprende entrambi i significati. Le informazioni biometriche stanno sostituendo sempre più le password per identificare e verificare gli utenti. È più sicuro e spesso più pratico sia per l'utente che per l'amministratore.

I sensori vengono usati per acquisire informazioni biometriche. Le informazioni vengono acquisite dal sensore come campione biometrico. Un singolo esempio contiene dati che rappresentano una singola caratteristica biometrica per un singolo utente. Viene mediata la media di più esempi per creare un modello biometrico e il modello viene archiviato in modo sicuro. Successivamente, un esempio di un utente sconosciuto viene confrontato con i modelli archiviati per stabilire e verificare l'identità dell'utente. Il Windows biometrico, che fa parte di Windows Biometric Framework (WBF), offre le funzionalità seguenti. che è possibile sfruttare utilizzando l'API di WBF.

-   Acquisisce campioni biometrici e li utilizza per creare un modello.
-   Salva e recupera in modo sicuro i modelli biometrici.
-   Mappe ogni modello in un identificatore univoco, ad esempio un GUID o un SID.

È anche possibile usare questa API per estendere il framework e creare adattatori di sensori biometrici, motori corrispondenti e componenti di archiviazione. Per altre informazioni sulla creazione di adattatori del sensore, sui motori corrispondenti e sui componenti di archiviazione, vedere [Creazione di plug-in dell'adattatore.](creating-adapter-plug-ins.md)

## <a name="core-platform-components"></a>Componenti principali della piattaforma

### <a name="windows-biometric-driver-interface-wbdi"></a>Windows Interfaccia del driver biometrico (WBDI)

WBDI è un'interfaccia di programmazione che un driver biometrico può usare per esporre il dispositivo biometrico tramite Windows Biometric Service (WBS). È possibile implementare un driver WBDI usando qualsiasi tecnologia di driver supportata, inclusi i seguenti. È tuttavia consigliabile usare UMDF quando possibile per migliorare la qualità del driver e la stabilità del sistema.

-   User Mode Driver Framework (UMDF)
-   Kernel Mode Driver Framework (KMDF)
-   Windows Modello di driver (WDM)

Un driver biometrico WBDI deve supportare anche il GUID dell'interfaccia del driver WBDI e tutti i controlli I/O obbligatori (IOCTL). Gli sviluppatori di driver devono esaminare la documentazione e il codice di esempio in Windows Driver Kit (WDK).

### <a name="windows-biometric-service-wbs"></a>Windows Servizio biometrico (WBS)

Il Windows Biometric Service gestisce i driver biometrici installati e supporta l'API Windows Biometric Framework per fornire l'accesso dei dispositivi alle applicazioni client. WBS esegue le funzioni seguenti:

-   Protegge la riservatezza degli utenti separando le applicazioni client dai dati biometrici.
-   Protegge i dati biometrici da applicazioni client senza privilegi richiedendo che le applicazioni oscivano accedere ai dati usando identificatori univoci.
-   Usa un componente software denominato [unità biometrica per](/previous-versions//dd401512(v=vs.85)) esporre le funzionalità di un particolare dispositivo biometrico tramite un'interfaccia standardizzata.
-   Gestisce le unità biometriche raggruppandole in pool di sensori di sistema, privati o non [assegnati.](sensor-pools.md)
-   Supporta l'uso di adattatori unità [biometriche](/previous-versions//dd401508(v=vs.85)) per i dispositivi fisici privi di funzionalità di elaborazione o archiviazione di onboarding.

### <a name="windows-biometric-framework-api"></a>Windows Biometric Framework API

L Windows'API Biometric Framework consente di creare applicazioni client in grado di interagire con il servizio biometrico Windows per eseguire le azioni seguenti:

-   Identificare e verificare gli utenti.
-   Individuare i dispositivi biometrici ed eseguire query sulle relative funzionalità.
-   Gestire le sessioni e monitorare gli eventi.

## <a name="user-experience-components"></a>Componenti dell'esperienza utente

### <a name="discovery-points"></a>Punti di individuazione

Gli utenti finali possono individuare i dispositivi biometrici in uno dei modi seguenti:

-   Digitando le parole biometria, impronta digitale, viso o altre frasi correlate nella casella di testo Avvia ricerca per avviare il pannello di controllo dei dispositivi biometrici. L'elenco dei risultati per la biometria può contenere elementi come i seguenti in un'Windows 10 immagine.
    -   Configurare l'accesso tramite impronta digitale
    -   Configurare l'accesso viso

### <a name="supported-scenarios"></a>Scenari Supportati

Sono supportati gli scenari indicati di seguito:

-   Gli utenti possono accedere a un computer locale, a un gruppo di lavoro o a un dominio usando un lettore di impronte digitali o una fotocamera A/A incentrata sul viso.
-   Un utente con privilegi amministrativi può elevare le applicazioni tramite controllo dell'account utente usando un'impronta digitale o un viso.

## <a name="management-components"></a>Componenti di gestione

Un sistema biometrico può essere gestito usando Criteri di gruppo gestione dei dispositivi mobili (MDM).

### <a name="biometric-system-management"></a>Gestione dei sistemi biometrici

È possibile gestire le funzionalità biometriche usando Criteri di gruppo o MDM. Criteri di gruppo possibile usare ulteriormente per eseguire le azioni seguenti:

-   Specificare il periodo di timeout per il cambio rapido utente, se implementato dall'ISV.
-   Impedire l'installazione del dispositivo biometrico.
-   Forzare la rimozione dei driver per i dispositivi biometrici.
-   Disabilitare il servizio biometrico.

 

 