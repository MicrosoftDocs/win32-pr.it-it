---
title: Compatibilità e affidabilità
description: Windows 7 è progettato per essere eseguito sullo stesso hardware di Windows Vista e per essere compatibile con le applicazioni e i driver di dispositivo che funzionano con Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e9686c732c94b4b99408d0fd6e24f84079ee9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300239"
---
# <a name="compatibility-and-reliability"></a>Compatibilità e affidabilità

Windows 7 è progettato per essere eseguito sullo stesso hardware di Windows Vista e per essere compatibile con le applicazioni e i driver di dispositivo che funzionano con Windows Vista.

Windows 7 è ancora la versione più affidabile di Windows. Progettato in base a una tecnologia migliorata, Windows 7 consente agli utenti di avviare, arrestare o sospendere i computer in modo affidabile senza doversi preoccupare della perdita di lavoro prezioso. Inoltre, Windows 7 rende più semplice che mai eseguire il backup e il ripristino dei dati in unità di rete o dischi digitali (DVD). Windows 7 migliora inoltre l'affidabilità e le prestazioni di stampa. Vedere le informazioni di riferimento sulla [qualità delle applicazioni di Windows 7](../win7appqual/windows-7-application-quality-cookbook.md).

## <a name="applications"></a>Applicazioni

Per garantire la compatibilità, Windows 7 è stato progettato in collaborazione ravvicinata con fornitori di software e produttori di PC. Il primo impegno ha permesso a Microsoft di creare un elenco completo delle applicazioni più diffuse. I cicli di test automatici garantiscono che i problemi di compatibilità vengano rilevati e risolti tempestivamente nel ciclo di sviluppo. Vedere [compatibilità delle applicazioni Windows](/windows/apps/desktop/).

## <a name="drivers"></a>Driver

La versione 7.0.0 di Windows Driver Kit (WDK) fornisce l'ambiente di compilazione, gli strumenti, la documentazione e gli esempi necessari agli sviluppatori per creare driver di qualità per Windows. Il 7.0.0 WDK supporta l'analisi statica del codice sorgente, usando PREfast per rilevare determinate classi di errori di codifica C e C++. PREfast include un componente driver specializzato, noto come PREfast for drivers (PFD), che rileva gli errori nel codice del driver in modalità kernel. Inoltre, WDK è stato migliorato annotando tutti i file di intestazione del kernel per il supporto di PFD. Sono stati aggiunti nuovi driver di esempio che illustrano nuove tecnologie e la documentazione è stata espansa.

Windows 7 supporta un'ampia gamma di prodotti software e hardware progettati per integrarsi perfettamente con la piattaforma. I driver creati per Windows Vista non devono richiedere l'aggiornamento per una corretta esecuzione in Windows 7. (Vedere [Kit driver Windows](/windows-hardware/drivers/)).

## <a name="devices"></a>Dispositivi

Windows 7 offre un supporto flessibile e affidabile per un'ampia gamma di applicazioni e dispositivi, inclusi lettori musicali, dispositivi di archiviazione, telefoni cellulari e altri tipi di dispositivi connessi. I test automatici di questi dispositivi vengono usati per garantire la corretta correzione dei problemi di compatibilità nelle fasi iniziali del ciclo di sviluppo. Vedere [nozioni fondamentali sulla classe di dispositivi Windows](https://www.microsoft.com/whdc/device/default.mspx).

## <a name="reliability-analysis-component"></a>Componente di analisi dell'affidabilità

Componente di analisi dell'affidabilità è un agente incorporato che fornisce informazioni dettagliate sull'esperienza utente relative all'utilizzo del sistema e all'affidabilità. Queste informazioni vengono esposte tramite un'interfaccia di Strumentazione gestione Windows (WMI), rendendole disponibili per l'utilizzo da parte di sistemi per lettori portatili. L'esposizione del Componente di analisi dell'affidabilità tramite un'interfaccia WMI consente agli sviluppatori di monitorare e analizzare le applicazioni, aumentando affidabilità e prestazioni.

Windows 7 usa il componente di analisi dell'affidabilità incorporato per calcolare un indice di affidabilità che fornisce informazioni sull'utilizzo e sulla stabilità complessive del sistema nel tempo. Il Componente di analisi dell'affidabilità tiene anche traccia di qualsiasi importante modifica al sistema che potrebbe avere un impatto sulla stabilità, ad esempio aggiornamenti di Windows e installazioni di applicazioni. È possibile utilizzare lo snap-in Monitoraggio affidabilità per visualizzare le tendenze nell'indice di affidabilità del sistema correlate a questi eventi potenzialmente destabilibili, semplificando la traccia di una modifica dell'affidabilità direttamente in un particolare evento. Vedere la [funzione MountVHD](/previous-versions/windows/desktop/msvs/mountvhd).

 

 