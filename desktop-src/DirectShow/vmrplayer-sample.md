---
description: Esempio di VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Esempio di VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c6281147e2c140541ade480e5b2a5e0f0a1d4146dde59b4871441b68fec6f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071915"
---
# <a name="vmrplayer-sample"></a>Esempio di VMRPlayer

## <a name="description"></a>Descrizione

Questo esempio usa il filtro Video Mixing Renderer 9 (VMR-9) per la fusione alfa di uno o due video in esecuzione e un'immagine statica.

## <a name="usage"></a>Utilizzo

Per aprire il primo video, scegliere **Apri flusso primario** dal menu **File.** Per aprire un secondo video, scegliere **Open Secondary Stream** (Apri flusso secondario) dal menu **File** (è prima necessario aprire il flusso primario). Per riprodurre il video, fare clic sul **pulsante** Riproduci.

È possibile impostare la posizione, le dimensioni e i valori alfa dei video selezionando **Primary Stream (Flusso** primario) o **Secondard Stream** (Flusso secondord) dal menu **VMR Properties (Proprietà VMR).**

Per aggiungere una bitmap statica sul video, scegliere **Static App Image** (Immagine app statica) dal menu VMR Properties (Proprietà **VMR)** e fare clic **sulla casella Display App Image (Visualizza immagine app).** È possibile usare la stessa finestra di dialogo per controllare la posizione, le dimensioni e il valore alfa della bitmap.

Per acquisire l'immagine video blended, scegliere **Capture Bitmap Image (Acquisisci immagine bitmap)** dal menu **VMR Properties (Proprietà VMR).**

È anche possibile specificare il flusso dell'immagine primaria dalla riga di comando:

**Nome file VMRPlayer** **/P** 

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi DirectShow SDK, installare la versione più recente di [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Campioni](directshow-samples.md)
</dt> </dl>

 

 



