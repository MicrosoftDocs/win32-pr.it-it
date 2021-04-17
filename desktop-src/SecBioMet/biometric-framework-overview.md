---
title: Panoramica di Biometric Framework
description: Il supporto nativo per i dispositivi biometrici è incorporato in Windows.
ms.assetid: 616ba95a-27a3-4eac-b802-5217954ed04e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f524437ba60f0ad5c1518225f91ff23c789a917
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473715"
---
# <a name="biometric-framework-overview"></a>Panoramica di Biometric Framework

Ogni persona ha caratteristiche univoche che possono essere usate per l'identificazione. In genere queste caratteristiche sono fisiche e includono tratti, come le impronte digitali, ma possono anche includere tratti comportamentali, ad esempio andamento e tipizzazione. Il termine biometria comprende entrambi i significati. Le informazioni biometriche stanno sempre sostituendo le password per identificare e verificare gli utenti. È più sicuro e spesso più comodo per utenti e amministratori.

I sensori vengono usati per acquisire le informazioni biometriche. Le informazioni vengono acquisite dal sensore come esempio biometrico. Un singolo campione contiene dati che rappresentano una singola caratteristica biometrica per un singolo utente. Per creare un modello biometrico viene calcolata la media di più campioni e il modello viene archiviato in modo sicuro. Successivamente, un campione di un utente sconosciuto viene confrontato con i modelli archiviati per stabilire e verificare l'identità dell'utente. Il servizio biometrico di Windows, parte del Windows Biometric Framework (WBF), fornisce le funzionalità seguenti. che è possibile sfruttare utilizzando l'API di WBF.

-   Acquisisce campioni biometrici e li utilizza per creare un modello.
-   Salva e recupera in modo sicuro i modelli biometrici.
-   Esegue il mapping di ogni modello a un identificatore univoco, ad esempio un GUID o un SID.

È anche possibile usare questa API per estendere il Framework e creare adattatori di sensori biometrici, motori di corrispondenza e componenti di archiviazione. Per ulteriori informazioni sulla creazione di adattatori di sensori, motori di corrispondenza e componenti di archiviazione, vedere [creazione di plug-](creating-adapter-plug-ins.md)in di adapter.

## <a name="core-platform-components"></a>Componenti della piattaforma di base

### <a name="windows-biometric-driver-interface-wbdi"></a>Interfaccia driver di Windows Biometric (WBDI)

WBDI è un'interfaccia di programmazione che può essere usata da un driver biometrico per esporre il dispositivo biometrico tramite il servizio Windows biometrico (WBS). È possibile implementare un driver WBDI usando qualsiasi tecnologia di driver supportata, incluse le seguenti. Si consiglia, tuttavia, di usare UMDF quando possibile per migliorare la qualità del driver e la stabilità del sistema.

-   Framework del driver della modalità utente (UMDF)
-   Framework driver in modalità kernel (KMDF)
-   Windows Driver Model (WDM)

Un driver WBDI Biometric deve supportare anche il GUID dell'interfaccia del driver WBDI e tutti i controlli I/O obbligatori (IOCTL). Gli sviluppatori di driver devono esaminare la documentazione e il codice di esempio in Windows Driver Kit (WDK).

### <a name="windows-biometric-service-wbs"></a>Servizio biometrico Windows (WBS)

Il servizio biometrico di Windows gestisce i driver biometrici installati e supporta l'API Windows Biometric Framework per fornire l'accesso ai dispositivi alle applicazioni client. WBS esegue le funzioni seguenti:

-   Protegge la riservatezza degli utenti separandoli tra le applicazioni client e i dati biometrici.
-   Protegge i dati biometrici dalle applicazioni client senza privilegi richiedendo che le applicazioni ottengano l'accesso ai dati usando identificatori univoci.
-   Usa un componente software denominato [unità biometrica](/previous-versions//dd401512(v=vs.85)) per esporre le funzionalità di un determinato dispositivo biometrico tramite un'interfaccia standardizzata.
-   Gestisce le unità biometriche raggruppando i [pool nei pool di sensori](sensor-pools.md)di sistema, privati o non assegnati.
-   Supporta l'uso degli [adattatori](/previous-versions//dd401508(v=vs.85)) di unità biometrici per i dispositivi fisici che non dispongono di funzionalità di elaborazione o di archiviazione onboard.

### <a name="windows-biometric-framework-api"></a>API Windows Biometric Framework

L'API Windows Biometric Framework consente di creare applicazioni client in grado di interagire con il servizio biometrico di Windows per eseguire le azioni seguenti:

-   Identificare e verificare gli utenti.
-   Individuare i dispositivi biometrici ed eseguire query sulle relative funzionalità.
-   Gestione delle sessioni e monitoraggio degli eventi.

## <a name="user-experience-components"></a>Componenti dell'esperienza utente

### <a name="discovery-points"></a>Punti di individuazione

Gli utenti finali possono individuare i dispositivi biometrici in uno dei modi seguenti:

-   Digitando le parole biometria, impronta digitale, viso o altre frasi correlate nella casella di testo Inizia ricerca per avviare il pannello di controllo dei dispositivi biometrici. L'elenco dei risultati per la biometria può contenere elementi come i seguenti in un'immagine di Windows 10.
    -   Configurare l'accesso con impronta digitale
    -   Configurare l'accesso viso

### <a name="supported-scenarios"></a>Scenari Supportati

Sono supportati gli scenari indicati di seguito:

-   Gli utenti possono accedere a un computer locale, un gruppo di lavoro o a un dominio usando un lettore di impronte digitali o la fotocamera IR incentrata sulla faccia.
-   Un utente con privilegi amministrativi può elevare le applicazioni attraverso il controllo dell'account utente usando un'impronta digitale o una faccia.

## <a name="management-components"></a>Componenti di gestione

Un sistema biometrico può essere gestito con Criteri di gruppo o gestione di dispositivi mobili (MDM).

### <a name="biometric-system-management"></a>Gestione del sistema biometrico

È possibile gestire le funzionalità biometriche usando Criteri di gruppo o MDM. Criteri di gruppo possibile utilizzare ulteriormente per eseguire le azioni seguenti:

-   Specificare il periodo di timeout per il cambio rapido utente, se implementato dall'ISV.
-   Impedisci l'installazione del dispositivo biometrico.
-   Forzare la rimozione dei driver per i dispositivi biometrici.
-   Disabilitare il servizio biometrico.

 

 