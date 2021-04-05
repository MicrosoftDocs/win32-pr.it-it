---
title: Interfacce IAVIStream e IAVIFile
description: Interfacce IAVIStream e IAVIFile
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Interfaccia IAVIStream
- Interfaccia IAVIFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856358"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Interfacce IAVIStream e IAVIFile

Le interfacce [**IAVIStream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) e [**IAVIFile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) contengono i metodi usati dai gestori di file e flussi. Il tipo di dati **PAVISTREAM** è un puntatore a un oggetto flusso AVI (tramite l'interfaccia **IAVIStream** ) e il tipo di dati **PAVIFILE** è un puntatore a un oggetto file AVI (tramite l'interfaccia **IAVIFile** ).

Per creare un puntatore a oggetti in C, allocare prima di tutto lo spazio per una struttura sufficientemente grande da contenere il puntatore alla tabella della funzione virtuale e agli altri membri dati. Creare una tabella di funzioni virtuali per i metodi per il tipo di flusso, quindi impostare il puntatore sulla tabella di funzioni virtuali sull'indirizzo della tabella della funzione virtuale.

 

 




