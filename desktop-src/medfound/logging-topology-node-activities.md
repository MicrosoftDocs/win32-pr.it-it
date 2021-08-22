---
description: Registrazione delle attività del nodo topologia
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Registrazione delle attività del nodo topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b2325b7f300ac7ebc9b11e442169ad81f5769a8b54ba0ecf4537d637a9e7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465521"
---
# <a name="logging-topology-node-activities"></a>Registrazione delle attività del nodo topologia

TopoEdit consente di raccogliere informazioni di registrazione per un nodo di trasformazione o un nodo di output di una topologia.

## <a name="to-setup-logging"></a>Per configurare la registrazione

1.  Nel riquadro **Topologia selezionare** un nodo di trasformazione o un nodo di output facendo clic su di esso.

2.  Scegliere **Spy** Selected **Node** dal menu Strumenti .

Durante la compilazione della topologia, tutte le chiamate al metodo nel nodo selezionato vengono registrate in un file di testo. Viene salvato nella cartella in cui si trova il file multimediale. Il file di log viene salvato con il nome del nodo e l'identificatore univoco del nodo della topologia. Ciò garantisce che nessun altro nodo scrive nel log. Per ottenere l'identificatore a livello di codice, chiamare [**IMFTopologyNode::GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).

Di seguito è riportato un estratto di un file di log.

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[TopoModifica](topoedit.md)
</dt> </dl>

 

 



