---
description: Windows Il componente di creazione dell'immagine (WIC) semplifica la gestione dei colori fornendo l'interfaccia IWICColorContext e l'interfaccia IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Panoramica della gestione dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a8c30074210a0a061fcbd26b05054591d2023805bfdff0848f0d7054dfe07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090050"
---
# <a name="color-management-overview"></a>Panoramica della gestione dei colori

Le immagini digitali provengono da e sono destinate a un'ampia gamma di dispositivi, ognuno dei quali ha una propria gamma dinamica e di gamma. Se un utente acquisisce la stessa scena in due fotocamere diverse, i colori nelle immagini risultanti non apparirebbero esattamente uguali, anche quando ne viene eseguito il rendering nello stesso dispositivo di output perché le funzionalità di gamut dei colori dei due dispositivi di origine erano diverse. Analogamente, la stessa immagine di cui viene eseguito il rendering in due dispositivi di destinazione diversi verrà visualizzata in modo diverso perché i dispositivi di destinazione hanno profili colori diversi. Per garantire la riproduzione coerente dei colori tra i dispositivi, è necessario creare un mapping dal profilo colori del dispositivo di origine al profilo colori del dispositivo di destinazione. La gestione dei colori cerca di produrre una corrispondenza visiva stretta e coerente ed è una funzionalità fondamentale per la creazione di immagini professionali.

La possibilità di riprodurre in modo coerente i colori tra scanner, monitor, stampanti e applicazioni sembra un obiettivo semplice, ma senza un sistema di gestione dei colori nel sistema operativo è difficile da raggiungere. Se ogni applicazione deve generare i propri profili colori, è quasi impossibile ottenere un interscambio di colori coerente durante il processo di pubblicazione, che include analisi, modifica e composizione, strumenti di verifica e distribuzione.

Windows Il componente di creazione dell'immagine (WIC) semplifica la gestione dei colori fornendo [**l'interfaccia IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e [**l'interfaccia IWICColorTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) È possibile ottenere un [**oggetto IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) usando [**IWICFactory::CreateColorTransformer.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer) [**IWICColorContext è**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) un'astrazione per il profilo colore del dispositivo. **IWICColorContext viene** inizializzato con un frame bitmap, il profilo colore del dispositivo di origine e il profilo colori del dispositivo di destinazione. Esegue la conversione del frame bitmap.

 

 



