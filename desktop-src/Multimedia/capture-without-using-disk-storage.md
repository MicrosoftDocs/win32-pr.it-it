---
title: Acquisisci senza usare archiviazione su disco
description: Acquisisci senza usare archiviazione su disco
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Messaggio WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298011"
---
# <a name="capture-without-using-disk-storage"></a>Acquisisci senza usare archiviazione su disco

È possibile utilizzare i servizi di acquisizione senza scrivere i dati in un file su disco utilizzando il messaggio di [**sequenza di WM \_ Cap \_ Sequence \_ nofile**](wm-cap-sequence-nofile.md) (o la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ). Questo messaggio è utile solo in combinazione con le funzioni di callback che consentono all'applicazione di usare direttamente i dati video e audio. Ad esempio, le applicazioni di videoconferenza potrebbero utilizzare questo messaggio per ottenere i frame video di streaming. Le funzioni di callback trasferiscono le immagini acquisite al computer remoto.

 

 




