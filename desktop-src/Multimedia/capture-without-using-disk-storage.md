---
title: Acquisire senza usare dischi Archiviazione
description: Acquisire senza usare dischi Archiviazione
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE messaggio
- Macro capCaptureSequenceNoFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea708bd99cc2c325623eb53d734fadb2acdd0112e3a727fae9bfa741b8d301e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691621"
---
# <a name="capture-without-using-disk-storage"></a>Acquisire senza usare dischi Archiviazione

È possibile usare i servizi di acquisizione senza scrivere i dati in un file su disco usando il messaggio [**WM \_ CAP SEQUENCE \_ \_ NOFILE**](wm-cap-sequence-nofile.md) (o la macro [**capCaptureSequenceNoFile).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) Questo messaggio è utile solo in combinazione con le funzioni di callback che consentono all'applicazione di usare direttamente i dati audio e video. Ad esempio, le applicazioni di videoconferenza potrebbero usare questo messaggio per ottenere fotogrammi video in streaming. Le funzioni di callback trasferirebbero le immagini acquisite nel computer remoto.

 

 




