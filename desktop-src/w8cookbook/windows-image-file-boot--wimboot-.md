---
title: Avvio file immagine Windows (WimBoot)
description: Avvio file immagine Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734642"
---
# <a name="windows-image-file-boot-wimboot"></a>Avvio file immagine Windows (WimBoot)

## <a name="platform"></a>Piattaforma

**Client:** Windows 8.1  

## <a name="description"></a>Descrizione

WimBoot è un metodo alternativo per la distribuzione di Windows da parte degli OEM. Una distribuzione di WimBoot avvia ed esegue Windows direttamente da un file di immagine Windows compresso (WIM). Questo file WIM non è modificabile e l'accesso a esso è gestito da un nuovo driver di filtro file system (WoF.sys).

Il risultato è una riduzione significativa dello spazio su disco necessario per l'installazione di Windows.

## <a name="manifestations"></a>Manifestazioni

La maggior parte delle applicazioni deve essere completamente inalterata da WimBoot. Potrebbero essere interessate solo le applicazioni che accedono e sbloccano i file di sistema o i file pre-caricati per l'accesso in scrittura. Poiché il file WIM non è modificabile, gli aggiornamenti (ovvero i file di sistema o pre-caricati) vengono archiviati semplicemente nella partizione C: \\ .

Se un'applicazione ha sbloccato l'accesso in scrittura per tutti i file di sistema con supporto WIM e i file precaricati, il risparmio fornito da WimBoot verrebbe perso completamente, perché tutti questi file verrebbero decompressi e inseriti nel volume C: \\ .

Inoltre, le applicazioni di backup e ripristino devono essere in grado di riconoscere le distribuzioni di WimBoot, poiché il file WIM è presente in una partizione separata. ovvero, durante il backup, è necessario salvare entrambe le partizioni C: \\ e Wim ed è necessario ripristinare entrambe insieme.

## <a name="solution"></a>Soluzione

Sono state introdotte nuove API che consentono alle applicazioni di eseguire query direttamente se un volume o un file specifico è supportato da un file WIM. Queste informazioni consentono alle applicazioni di prendere decisioni appropriate, ad esempio l'apertura di questi file solo per l'accesso in lettura o l'identificazione di volumi o partizioni di cui è necessario eseguire il backup e il ripristino insieme.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Test di compatibilità, prestazioni, affidabilità o usabilità

Gli sviluppatori di applicazioni devono testare il software e gli scenari corrispondenti in un sistema WimBoot, soprattutto se queste applicazioni accedono a file di sistema o precaricati. È necessario prestare particolare attenzione a una riduzione significativa dello spazio disponibile su disco dopo il completamento di uno scenario.

 

 




