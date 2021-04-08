---
description: Esempio VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Esempio VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880042"
---
# <a name="vmrplayer-sample"></a>Esempio VMRPlayer

## <a name="description"></a>Descrizione

Questo esempio usa il filtro video mixaggio 9 (VMR-9) per la fusione alfa di uno o due video in esecuzione e un'immagine statica.

## <a name="usage"></a>Utilizzo

Per aprire il primo video, scegliere **Apri flusso primario** dal menu **file** . Per aprire un secondo video, scegliere **Apri flusso secondario** dal menu **file** (è necessario prima aprire il flusso primario). Per riprodurre il video, fare clic sul pulsante **Riproduci** .

È possibile impostare la posizione, le dimensioni e i valori alfa dei video selezionando **flusso primario** o **flusso secondard** dal menu **Proprietà VMR** .

Per aggiungere una bitmap statica sul video, scegliere **immagine app statica** dal menu **proprietà di VMR** e fare clic sulla casella **Visualizza immagine dell'app** . È possibile utilizzare la stessa finestra di dialogo per controllare la posizione, le dimensioni e il valore alfa della bitmap.

Per acquisire l'immagine del video mescolato, scegliere **Acquisisci immagine bitmap** dal menu **Proprietà VMR** .

È anche possibile specificare il flusso di immagini primarie dalla riga di comando:

**VMRPlayer** **/p** *nomefile*

## <a name="downloading-the-sample"></a>Download dell'esempio

Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di DirectShow](directshow-samples.md)
</dt> </dl>

 

 



