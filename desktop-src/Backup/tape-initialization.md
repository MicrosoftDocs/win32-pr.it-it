---
title: Inizializzazione del nastro
description: Per creare un handle di un dispositivo nastro, un'applicazione deve utilizzare la funzione CreateFile. Questo handle viene usato nelle operazioni successive sul nastro nel dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Backup inizializzazione nastro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473678"
---
# <a name="tape-initialization"></a>Inizializzazione del nastro

Per creare un handle di un dispositivo nastro, un'applicazione deve utilizzare la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Questo handle viene usato nelle operazioni successive sul nastro nel dispositivo.

Prima di scrivere su un nastro, un'applicazione deve essere formattata in base alle esigenze dell'applicazione e alle funzionalità dell'unità nastro utilizzata. La funzione [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) riformatta un nastro, creando un determinato numero di partizioni di una dimensione specificata.

La funzione [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara un nastro per l'accesso o la rimozione. Questa funzione può caricare, scaricare, bloccare o sbloccare un nastro. Questa funzione può anche eseguire il tensionamento del nastro spostando il nastro alla fine del nastro e tornando all'inizio.

Per recuperare e impostare le informazioni su un'unità nastro e nastro, un'applicazione utilizza le funzioni [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)e [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .

[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera le informazioni che descrivono un nastro o un'unità nastro. Le informazioni sul nastro includono tipo, densità e dimensione del blocco del nastro; il numero di partizioni sul nastro; quantità di nastri rimanenti; E così via. Le informazioni sulle unità nastro includono le dimensioni del blocco predefinite dell'unità, il numero massimo di partizioni e le funzionalità supportate.

[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) imposta la dimensione del blocco del nastro o imposta i flag di unità nastro che indicano se l'unità supporta la correzione degli errori hardware, la compressione dei dati, il riempimento dei dati o qualsiasi combinazione dei tre.

[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica se l'unità nastro è pronta per l'elaborazione dei comandi del nastro.

 

 