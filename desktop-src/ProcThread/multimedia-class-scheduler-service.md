---
description: Il servizio Utilità di pianificazione classi multimediali (MMCSS) consente alle applicazioni multimediali di garantire che la loro elaborazione sensibile al tempo riceva l'accesso in ordine di priorità alle risorse della CPU.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Servizio Utilità di pianificazione classi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80656276af30495c084d0964534a04e11896bcd2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968886"
---
# <a name="multimedia-class-scheduler-service"></a>Servizio Utilità di pianificazione classi multimediali

Il servizio Utilità di pianificazione classi multimediali (MMCSS) consente alle applicazioni multimediali di garantire che la loro elaborazione sensibile al tempo riceva l'accesso in ordine di priorità alle risorse della CPU. Questo servizio consente alle applicazioni multimediali di utilizzare il maggior quantità possibile di CPU senza negare risorse della CPU alle applicazioni con priorità più bassa.

MMCSS utilizza le informazioni archiviate nel registro di sistema per identificare le attività supportate e determinare la priorità relativa dei thread che eseguono queste attività. Ogni thread che esegue lavoro correlato a una determinata attività chiama la funzione [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) o [**AVSETMMTHREADCHARACTERISTICS**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) per informare MMCSS che sta lavorando su tale attività.

Per un esempio di un programma che usa MMCSS, vedere [flussi in modalità esclusiva](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 e Windows XP:** MMCSS non è disponibile.

## <a name="registry-settings"></a>Impostazioni del Registro di sistema

Le impostazioni MMCSS vengono archiviate nella seguente chiave del registro di sistema:

**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Multimedia \\ systemprofile**

Questa chiave contiene un valore **reg \_ DWORD** denominato **SystemResponsiveness** che determina la percentuale di risorse della CPU da garantire per le attività con priorità bassa. Se, ad esempio, questo valore è 20, il 20% delle risorse della CPU viene riservato per le attività con priorità bassa. Si noti che i valori che non sono divisibile in modo uniforme per 10 vengono arrotondati al multiplo più vicino di 10. Anche il valore 0 viene considerato come 10.

La chiave contiene anche una sottochiave denominata **Tasks** che contiene l'elenco delle attività. Per impostazione predefinita, Windows supporta le attività seguenti:

-   **Audio**
-   **Acquisire**
-   **Distribuzione**
-   **Giochi**
-   **Riproduzione**
-   **Audio Pro**
-   **Gestione finestre**

Gli OEM possono aggiungere ulteriori attività, se necessario.

Ogni chiave dell'attività contiene il set di valori seguente che rappresenta le caratteristiche da applicare ai thread associati all'attività.

| Valore                   | Formato         | Valori possibili                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Affinità**            | **REG \_ DWORD** | Maschera di maschera che indica l'affinità del processore. Sia 0x00 che 0xFFFFFFFF indicano che l'affinità del processore non viene utilizzata.                                                                                                                                                                                                                                                 |
| **Solo sfondo**     | **REG \_ SZ**    | Indica se si tratta di un'attività in background (nessuna interfaccia utente). I thread di un'attività in background non cambiano a causa di una modifica nello stato attivo della finestra. Questo valore può essere impostato su true o false.                                                                                                                                                                            |
| **BackgroundPriority**  | **REG \_ DWORD** | Priorità di sfondo. L'intervallo di valori è 1-8.                                                                                                                                                                                                                                                                                                                    |
| **Frequenza di clock**          | **REG \_ DWORD** | Hint utilizzato da MMCSS per determinare la granularità della pianificazione delle risorse del processore. **Windows Server 2008 e Windows Vista:** Frequenza di clock massima garantita utilizzata dal sistema se un thread unisce questa attività, in intervalli di 100 nanosecondi. A partire da Windows 7 e Windows Server 2008 R2, questa garanzia è stata rimossa per ridurre il consumo di energia del sistema.<br/> |
| **Priorità GPU**        | **REG \_ DWORD** | Priorità della GPU. L'intervallo di valori è 0-31. Questa priorità non è ancora usata.                                                                                                                                                                                                                                                                                           |
| **Priorità**            | **REG \_ DWORD** | Priorità dell'attività. L'intervallo di valori è 1 (bassa) a 8 (alto). Per le attività con una **categoria di pianificazione** elevata, questo valore viene sempre considerato come 2.<br/>                                                                                                                                                                                                           |
| **Categoria di pianificazione** | **REG \_ SZ**    | Categoria di pianificazione. Questo valore può essere impostato su alto, medio o basso.                                                                                                                                                                                                                                                                                                 |
| **Priorità SFIO**       | **REG \_ SZ**    | Priorità di I/O pianificata. Questo valore può essere impostato su Idle, low, Normal o High. Questo valore non viene utilizzato.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Per conservare il potere, le applicazioni non devono impostare la risoluzione del timer a livello di sistema su un valore ridotto, a meno che non sia assolutamente necessario. Per ulteriori informazioni, vedere [prestazioni](../win7devguide/performance.md) nella [Guida per gli sviluppatori di Windows 7](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Priorità dei thread

MMCSS incrementa la priorità dei thread che lavorano sulle attività multimediali a priorità alta.

MMCSS determina la priorità di un thread usando i fattori seguenti:

-   Priorità di base dell'attività.
-   Parametro *Priority* della funzione [**AvSetMmThreadPriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority) .
-   Indica se l'applicazione è in primo piano.
-   Quantità di tempo della CPU utilizzata dai thread in ogni categoria.

MMCSS imposta la priorità dei thread client a seconda della categoria di pianificazione.

| Category | Priorità | Descrizione                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Alto     | 23-26    | Questi thread vengono eseguiti con una priorità di thread inferiore a determinate attività a livello di sistema. Questa categoria è progettata per le attività audio Pro. |
| Medio   | 16-22    | Questi thread fanno parte dell'applicazione in primo piano.                                                                      |
| Basso      | 8-15     | Questa categoria contiene il resto dei thread. Se necessario, viene garantita una percentuale minima delle risorse della CPU.           |
|          | 1-7      | Questi thread hanno usato la quota di risorse della CPU. Possono continuare a funzionare se nessun thread con priorità bassa è pronto per l'esecuzione.                |



 

 

 
