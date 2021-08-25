---
title: Dimensioni dell'indice
description: Dimensioni dell'indice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9742edb1aa73c7b77a56ef3ab2a29a5ea14a1e70351bec1ecb49507bbd0bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784681"
---
# <a name="index-size"></a>Dimensioni dell'indice

Ogni file AVI usa un indice di una dimensione specificata per individuare i blocchi di dati audio e video all'interno del file. Una voce nell'indice individua un frame video o un buffer audio waveform. Di conseguenza, il valore delle dimensioni dell'indice imposta indirettamente il limite superiore per il numero di frame che possono essere acquisiti in un file.

È possibile recuperare le dimensioni dell'indice corrente usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Le dimensioni dell'indice corrente vengono archiviate **nel membro dwIndexSize** della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) È possibile specificare una nuova dimensione di indice come valore di **dwIndexSize** e quindi inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Le dimensioni predefinite dell'indice sono 34.952 voci, consentendo 32.000 fotogrammi e un numero proporzionale di buffer audio.

 

 




