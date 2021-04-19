---
description: Windows Imaging Component (WIC) semplifica la gestione dei colori fornendo l'interfaccia IWICColorContext e l'interfaccia IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Panoramica sulla gestione dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1552375ee896173ba8d1fdbf4a9ae19c2af6e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317895"
---
# <a name="color-management-overview"></a>Panoramica sulla gestione dei colori

Le immagini digitali provengono da e sono destinate a una vasta gamma di dispositivi, ognuno dei quali ha una gamma e un intervallo dinamico specifici. Se un fotografo doveva acquisire la stessa scena su due fotocamere diverse, i colori delle immagini risultanti non venivano visualizzati esattamente allo stesso modo, anche quando ne viene eseguito il rendering sullo stesso dispositivo di output perché le funzionalità della gamma di colori dei due dispositivi di origine erano diverse. Analogamente, la stessa immagine sottoposta a rendering in due dispositivi di destinazione diversi verrà visualizzata in modo diverso perché i dispositivi di destinazione hanno profili colori diversi. Per garantire una riproduzione coerente dei colori tra dispositivi, è necessario creare un mapping dal profilo colori del dispositivo di origine al profilo colori del dispositivo di destinazione. La gestione dei colori cerca di produrre una corrispondenza visiva uniforme e coerente ed è una funzionalità fondamentale per la creazione di immagini professionali.

La possibilità di riprodurre costantemente i colori tra scanner, monitoraggi, stampanti e applicazioni sembra un semplice obiettivo, ma senza un sistema di gestione dei colori nel sistema operativo, è difficile da raggiungere. Se ogni applicazione è necessaria per generare profili colori personalizzati, è quasi impossibile ottenere un interscambio di colori coerente durante il processo di pubblicazione, che include l'analisi, la modifica e la composizione, la correzione e la distribuzione.

Windows Imaging Component (WIC) semplifica la gestione dei colori fornendo l'interfaccia [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e l'interfaccia [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) . È possibile ottenere un oggetto [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) usando [**IWICFactory:: CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer). [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) è un'astrazione per il profilo colori del dispositivo. **IWICColorContext** viene inizializzato con un frame bitmap, il profilo colori del dispositivo di origine e il profilo colori del dispositivo di destinazione. Esegue la conversione del frame bitmap.

 

 



