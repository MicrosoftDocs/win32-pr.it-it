---
description: Viene descritto come Windows 10 USA i set di API nelle operazioni del caricatore.
title: Funzionamento del caricatore dei set di API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "106320224"
---
# <a name="api-set-loader-operation"></a>Funzionamento del caricatore dei set di API

I [set di API](windows-apisets.md) si basano sul supporto del sistema operativo nel caricatore della libreria per introdurre efficacemente un reindirizzamento dello spazio dei nomi del modulo nel processo di associazione della libreria. Il [nome del contratto del set di API](windows-apisets.md#api-set-contract-names) viene usato dal caricatore della libreria per eseguire un reindirizzamento del runtime del riferimento a un file binario host di destinazione che ospita l'implementazione appropriata del set di API.

Quando il caricatore rileva una dipendenza da un'API impostata in fase di esecuzione, il caricatore consulta i dati di configurazione nell'immagine per identificare il file binario host per un set di API. Questi dati di configurazione sono definiti **schema del set di API**. Lo schema viene assemblato come una proprietà del sistema operativo e il mapping tra i set di API e i file binari può variare a seconda dei file binari inclusi in un determinato dispositivo. Lo schema consente di instradare correttamente una funzione importata in un singolo file binario su dispositivi diversi, anche se i nomi dei moduli dell'host binario sono stati rinominati o completamente sottoposti a refactoring in diversi dispositivi Windows.

Windows 10 supporta due tecniche standard per l'utilizzo e l'interfaccia con i set di API: l' **invio diretto** e l' **invio inverso**.

### <a name="direct-forwarding"></a>Inoltri diretti

In questa configurazione, il codice consumer importa direttamente il nome del modulo set di API. Questa importazione viene risolta in un'unica operazione ed è il metodo più efficiente con il minor sovraccarico. A livello concettuale, questa risoluzione può puntare a binari diversi in dispositivi Windows 10 diversi, come illustrato nell'esempio seguente:

Set di API importati: **api-feature1-l1-1-0.dll**
-  **feature1.dll** > PC Windows
-  HoloLens- **feature1_holo.dll** >
-  > **feature1_iot.dll**

Poiché i mapping vengono conservati in un archivio dati dello schema personalizzato, significa che il nome di un set di API che termina con **. dll** non fa riferimento direttamente a un file su disco. La parte **dll** del nome del set di API è solo una convenzione richiesta dal caricatore. Il nome del set di API è più simile a un alias o a un nome virtuale per un file DLL fisico. Questo rende il nome portabile nell'intero intervallo di dispositivi Windows 10.

### <a name="reverse-forwarding"></a>Inoltri inverso

Sebbene i nomi dei set di API forniscano uno spazio dei nomi stabile per i moduli tra i dispositivi, non è sempre consigliabile convertire ogni file binario in questo nuovo sistema. È ad esempio possibile che un'applicazione sia stata usata per molti anni e che la ricompilazione dei file binari dell'applicazione potrebbe non essere fattibile. Inoltre, è possibile che alcune applicazioni debbano continuare a essere eseguite nei sistemi compilati prima dell'introduzione di specifici set di API.

Per supportare questo livello di compatibilità, viene fornito un sistema di *server d'inoltri* in tutti i dispositivi Windows 10 che coprono un subset della superficie dell'API Win32. Questi server d'utilità usano i nomi dei moduli introdotti nei PC Windows e sfruttano il sistema di set di API per garantire la compatibilità tra tutti i dispositivi Windows 10.

Il comportamento dell'operazione del caricatore è analogo al seguente:

1.  In un dispositivo diverso da un PC Windows, il caricatore presenta una dipendenza legacy del nome del modulo PC Windows che non è presente nel dispositivo.
2.  Il caricatore individua un server d'installazione del set di API per questo modulo e lo carica in memoria.
3.  Il server d'esecuzione dispone di un mapping per il set di API per la funzione specificata chiamata.
4.  Il caricatore trova il file binario host appropriato per il dispositivo specificato.

Concettualmente, il mapping ha un aspetto simile al seguente:

DLL importata: **feature1.dll**
- **feature1.dll** > PC Windows
- HoloLens-> **feature1.dll** server d'avanzamento-> **api-feature1-l1-1-0.dll**  ->  **feature1_holo.dll**
- > **feature1.dll** server d'avanzamento-> **api-feature1-l1-1-0.dll**  ->  **feature1_iot.dll**

Il risultato finale è funzionalmente identico all'esecuzione [diretta](#direct-forwarding), ma viene eseguita in modo da ottimizzare la compatibilità delle applicazioni.

> [!NOTE]
> L'avanzamento inverso fornisce la copertura solo per un subset della superficie dell'API Win32. Non consente l'esecuzione di applicazioni destinate alle versioni desktop di Windows 10 in tutti i dispositivi Windows 10.
