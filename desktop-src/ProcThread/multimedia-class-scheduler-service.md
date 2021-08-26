---
description: Il servizio Utilità di pianificazione classi multimediali (MMCSS) consente alle applicazioni multimediali di garantire che l'elaborazione sensibile al tempo riceva l'accesso con priorità alle risorse della CPU.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Servizio Utilità di pianificazione classi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0744883180c361d5656cf7c182f538d93617be7f6bbdc6a05ff93efa732b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032441"
---
# <a name="multimedia-class-scheduler-service"></a>Servizio Utilità di pianificazione classi multimediali

Il servizio Utilità di pianificazione classi multimediali (MMCSS) consente alle applicazioni multimediali di garantire che l'elaborazione sensibile al tempo riceva l'accesso con priorità alle risorse della CPU. Questo servizio consente alle applicazioni multimediali di utilizzare il maggior numero possibile di CPU senza negare le risorse della CPU alle applicazioni con priorità inferiore.

MMCSS usa le informazioni archiviate nel Registro di sistema per identificare le attività supportate e determinare la priorità relativa dei thread che eseguono queste attività. Ogni thread che esegue operazioni correlate a una determinata attività chiama la funzione [**AvSetMmMaxThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) o [**AvSetMmThreadCharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) per informare MMCSS che sta lavorando a tale attività.

Per un esempio di programma che usa MMCSS, vedere [Exclusive-Mode Flussi](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 e Windows XP:** MMCSS non è disponibile.

## <a name="registry-settings"></a>Impostazioni del Registro di sistema

Le impostazioni di MMCSS vengono archiviate nella chiave del Registro di sistema seguente:

**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion Multimedia \\ \\ SystemProfile**

Questa chiave contiene un **valore \_ DWORD REG** denominato **SystemResponsiveness** che determina la percentuale di risorse CPU che devono essere garantite alle attività con priorità bassa. Ad esempio, se questo valore è 20, il 20% delle risorse della CPU è riservato alle attività con priorità bassa. Si noti che i valori non divisibile in modo uniforme per 10 vengono arrotondati per es. Anche il valore 0 viene considerato come 10.

La chiave contiene anche una sottochiave denominata **Tasks** che contiene l'elenco di attività. Per impostazione predefinita, Windows le attività seguenti:

-   **Audio**
-   **Acquisire**
-   **Distribuzione**
-   **Giochi**
-   **Riproduzione**
-   **Pro Audio**
-   **Gestione finestre**

Gli OEM possono aggiungere altre attività in base alle esigenze.

Ogni chiave dell'attività contiene il set di valori seguente che rappresentano le caratteristiche da applicare ai thread associati all'attività.

| Valore                   | Formato         | Valori possibili                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Affinità**            | **REG \_ DWORD** | Maschera di bit che indica l'affinità del processore. Sia 0x00 che 0xFFFFFFFF che l'affinità del processore non viene usata.                                                                                                                                                                                                                                                 |
| **Solo in background**     | **REG \_ SZ**    | Indica se si tratta di un'attività in background (nessuna interfaccia utente). I thread di un'attività in background non cambiano a causa di una modifica dello stato attivo della finestra. Questo valore può essere impostato su True o False.                                                                                                                                                                            |
| **BackgroundPriority**  | **REG \_ DWORD** | Priorità in background. L'intervallo di valori è compreso tra 1 e 8.                                                                                                                                                                                                                                                                                                                    |
| **Frequenza di clock**          | **REG \_ DWORD** | Hint usato da MMCSS per determinare la granularità della pianificazione delle risorse del processore. **Windows Server 2008 e Windows Vista:** Frequenza di clock massima garantita che il sistema usa se un thread aggiunge questa attività, a intervalli di 100 nanosecondi. A partire da Windows 7 e Windows Server 2008 R2, questa garanzia è stata rimossa per ridurre il consumo di energia del sistema.<br/> |
| **Priorità GPU**        | **REG \_ DWORD** | Priorità della GPU. L'intervallo di valori è compreso tra 0 e 31. Questa priorità non è ancora usata.                                                                                                                                                                                                                                                                                           |
| **Priorità**            | **REG \_ DWORD** | Priorità dell'attività. L'intervallo di valori è compreso tra 1 (basso) e 8 (alto). Per le attività con **una categoria di** pianificazione alta, questo valore viene sempre considerato 2.<br/>                                                                                                                                                                                                           |
| **Categoria di pianificazione** | **REG \_ SZ**    | Categoria di pianificazione. Questo valore può essere impostato su Alto, Medio o Basso.                                                                                                                                                                                                                                                                                                 |
| **Priorità SFIO**       | **REG \_ SZ**    | Priorità di I/O pianificata. Questo valore può essere impostato su Idle, Low, Normal o High. Questo valore non viene utilizzato.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Per risparmiare energia, le applicazioni non devono impostare la risoluzione del timer a livello di sistema su un valore ridotto, a meno che non sia assolutamente necessario. Per altre informazioni, vedere [Performance](../win7devguide/performance.md) in the [Windows 7 Developers Guide](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Priorità dei thread

MMCSS aumenta la priorità dei thread che lavorano su attività multimediali ad alta priorità.

MMCSS determina la priorità di un thread usando i fattori seguenti:

-   Priorità di base dell'attività.
-   Parametro *Priority* della [**funzione AvSetMmThreadPriority.**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)
-   Indica se l'applicazione è in primo piano.
-   Quantità di tempo cpu utilizzata dai thread in ogni categoria.

MMCSS imposta la priorità dei thread client a seconda della categoria di pianificazione.

| Category | Priorità | Descrizione                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Alto     | 23-26    | Questi thread vengono eseguiti con una priorità del thread inferiore rispetto solo a determinate attività a livello di sistema. Questa categoria è progettata per le Pro audio. |
| Medio   | 16-22    | Questi thread fanno parte dell'applicazione in primo piano.                                                                      |
| Basso      | 8-15     | Questa categoria contiene il resto dei thread. È garantita una percentuale minima delle risorse della CPU, se necessario.           |
|          | 1-7      | Questi thread hanno usato la quota di risorse CPU. Possono continuare a essere eseguiti se non sono pronti per l'esecuzione thread con priorità bassa.                |



 

 

 
