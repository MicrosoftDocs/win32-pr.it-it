---
title: Granularità dei blocchi video e audio
description: Granularità dei blocchi video e audio
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- File AVI, granularità dei blocchi
- Classe AVICap, blocchi filler
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955585"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularità dei blocchi video e audio

La granularità del blocco è una dimensione del blocco logico per un file AVI usato per la scrittura e il recupero di blocchi di dati audio e video. Quando si scrivono blocchi audio e video su disco, AVICap aggiunge blocchi di riempimento (blocchi "spazzatura") necessari per riempire ogni blocco logico di dati.

È possibile recuperare l'impostazione di granularità del blocco corrente usando il messaggio di [**installazione della sequenza di WM \_ Cap \_ \_ \_ Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). La granularità del blocco corrente viene archiviata nel membro **wChunkGranularity** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . È possibile specificare una nuova granularità dei blocchi come valore di **wChunkGranularity** , quindi inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ di set di WM Cap**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). È anche possibile specificare zero per questo membro per impostare la granularità dei blocchi sulle dimensioni del settore del disco.

 

 




