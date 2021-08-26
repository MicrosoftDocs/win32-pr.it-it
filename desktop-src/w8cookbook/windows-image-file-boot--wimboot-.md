---
title: Windows Avvio del file di immagine (WimBoot)
description: Windows Avvio del file di immagine (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a230188c3b13317d8176d8209cf5e38026c3b6f161be7ffe0c2ed760976ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932121"
---
# <a name="windows-image-file-boot-wimboot"></a>Windows Avvio del file di immagine (WimBoot)

## <a name="platform"></a>Piattaforma

**Client:** Windows 8.1  

## <a name="description"></a>Descrizione

WimBoot è un modo alternativo per gli OEM di distribuire Windows. Una distribuzione WimBoot viene avviato ed Windows direttamente da un file di immagine Windows compresso (WIM). Questo file WIM non è modificabile e l'accesso ad esso è gestito da un nuovo driver di filtro file system (WoF.sys).

Il risultato è una riduzione significativa dello spazio su disco necessario per installare Windows.

## <a name="manifestations"></a>Manifestazioni

La maggior parte delle applicazioni non deve essere influenzata completamente da WimBoot. Possono essere interessate solo le applicazioni che accedono e sbloccano file di sistema o file precaricati per l'accesso in scrittura. Poiché il file WIM non è modificabile, gli aggiornamenti ad esso (ovvero file di sistema o precaricati) vengono semplicemente archiviati nella partizione \\ C:.

Se un'applicazione sblocca l'accesso in scrittura per tutti i file precaricati e di sistema supportati da WIM, i risparmi che WimBoot offre andrebbero completamente persi, perché tutti questi file verrebbero decompressi e inseriti nel \\ volume C:.

Inoltre, è necessario che le applicazioni di backup e ripristino siano a conoscenza delle distribuzioni WimBoot, in quanto wim è presente in una partizione separata. in altre informazioni, in caso di backup, è necessario salvare entrambe le partizioni C: e WIM ed entrambe \\ devono essere ripristinate insieme.

## <a name="solution"></a>Soluzione

Sono state introdotte nuove API che consentono alle applicazioni di eseguire query direttamente se un determinato volume o file è supportato da un file WIM. Queste informazioni consentono alle applicazioni di prendere decisioni appropriate, ad esempio l'apertura di questi file solo per l'accesso in lettura o l'identificazione di volumi/partizioni di cui è necessario eseguire il backup e il ripristino insieme.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Test di compatibilità, prestazioni, affidabilità o usabilità

Gli sviluppatori di applicazioni devono testare il software e i relativi scenari corrispondenti in un sistema WimBoot, soprattutto se queste applicazioni accedono al sistema o ai file precaricati. È necessario prestare particolare attenzione a una riduzione significativa dello spazio disponibile su disco dopo il completamento di uno scenario.

 

 




