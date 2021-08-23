---
title: Compatibilità e affidabilità
description: Windows 7 è progettato per l'esecuzione nello stesso hardware di Windows Vista e per essere compatibile con le applicazioni e i driver di dispositivo che funzionano con Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e42dbf564fc524fbfb620746cea84e387fbe9f76484ce9e0d87803f55dae4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706301"
---
# <a name="compatibility-and-reliability"></a>Compatibilità e affidabilità

Windows 7 è progettato per l'esecuzione nello stesso hardware di Windows Vista e per essere compatibile con le applicazioni e i driver di dispositivo che funzionano con Windows Vista.

Windows 7 è la versione più affidabile di Windows ancora. Progettato su una base tecnologica migliorata, Windows 7 consente agli utenti di avviare, arrestare o ibernare in modo affidabile i computer senza doversi preoccupare di perdere il lavoro prezioso. Inoltre, Windows 7 rende più semplice che mai eseguire il backup e il ripristino dei dati in unità di rete o DVD (Digital Video Disc). Windows 7 migliora anche l'affidabilità e le prestazioni della stampa. (Vedere [Windows 7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md).)

## <a name="applications"></a>Applicazioni

Per garantire la compatibilità, Windows 7 è stato progettato in stretta collaborazione con fornitori di software e produttori di PC. L'engagement anticipato ha consentito a Microsoft di creare un elenco completo delle applicazioni più usate. I cicli di test automatizzati garantiscono che i problemi di compatibilità siano rilevati e risolti nelle prime fasi del ciclo di sviluppo. Vedere [Compatibilità Windows'applicazione.](/windows/apps/desktop/)

## <a name="drivers"></a>Driver

Il Windows Driver Kit (WDK) versione 7.0.0 fornisce l'ambiente di compilazione, gli strumenti, la documentazione e gli esempi necessari per creare driver di qualità per Windows. WDK 7.0.0 supporta l'analisi statica del codice sorgente, usando PREfast per rilevare determinate classi di errori di codifica C e C++. PREfast include un componente driver specializzato, noto come PREfast for Drivers (PFD), che rileva gli errori nel codice del driver in modalità kernel. Inoltre, WDK è stato migliorato annotando tutti i file di intestazione del kernel per il supporto PFD. Sono stati aggiunti nuovi driver di esempio che illustrano le nuove tecnologie e la documentazione è stata ampliata.

Windows 7 supporta un'ampia gamma di prodotti software e hardware progettati per integrarsi senza problemi con la piattaforma. I driver creati per Windows Vista non devono richiedere l'aggiornamento per essere eseguiti correttamente in Windows 7. Vedere Windows [Driver Kit](/windows-hardware/drivers/).

## <a name="devices"></a>Dispositivi

Windows 7 offre un supporto flessibile e affidabile per un'ampia gamma di applicazioni e dispositivi, tra cui lettori musicali, dispositivi di archiviazione, telefoni cellulari e altri tipi di dispositivi connessi. Il test automatico di questi dispositivi viene usato per garantire che i problemi di compatibilità siano risolti nelle prime fasi del ciclo di sviluppo. Vedere [nozioni fondamentali Windows classe device.](https://www.microsoft.com/whdc/device/default.mspx)

## <a name="reliability-analysis-component"></a>Componente di analisi dell'affidabilità

Componente di analisi dell'affidabilità è un agente incorporato che fornisce informazioni dettagliate sull'esperienza utente relative all'utilizzo del sistema e all'affidabilità. Queste informazioni vengono esposte tramite un'interfaccia di Strumentazione gestione Windows (WMI), rendendole disponibili per l'utilizzo da parte di sistemi per lettori portatili. L'esposizione del Componente di analisi dell'affidabilità tramite un'interfaccia WMI consente agli sviluppatori di monitorare e analizzare le applicazioni, aumentando affidabilità e prestazioni.

Windows 7 usa il componente di analisi dell'affidabilità incorporato per calcolare un indice di affidabilità che fornisce informazioni sull'utilizzo e la stabilità complessive del sistema nel tempo. Il Componente di analisi dell'affidabilità tiene anche traccia di qualsiasi importante modifica al sistema che potrebbe avere un impatto sulla stabilità, ad esempio aggiornamenti di Windows e installazioni di applicazioni. È possibile usare lo snap-in Monitoraggio affidabilità per visualizzare le tendenze nell'indice di affidabilità del sistema correlate a questi eventi potenzialmente destabilizzanti, rendendo più semplice tracciare una modifica dell'affidabilità direttamente a un evento specifico. Vedere [La funzione MountVHD.](/previous-versions/windows/desktop/msvs/mountvhd)

 

 