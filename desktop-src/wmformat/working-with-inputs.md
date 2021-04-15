---
title: Utilizzo degli input
description: Utilizzo degli input
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK, utilizzo degli input
- Formato di sistemi avanzati (ASF), utilizzo degli input
- ASF (formato avanzato dei sistemi), utilizzo degli input
- profili, utilizzo di input
- flussi, utilizzo di input
- codec, utilizzo di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471115"
---
# <a name="working-with-inputs"></a>Utilizzo degli input

Proprio come la configurazione di flusso appropriata nel profilo è necessaria per ottenere il codec per comprimere un flusso, è inoltre necessario assicurarsi che il tipo di supporto non compresso passato al writer venga descritto accuratamente. A ogni codec Windows Media è associato un tipo di input predefinito, ma sono supportati diversi tipi di input. È possibile esaminare gli input supportati e selezionare quello che corrisponde ai dati. Il processo di utilizzo degli input viene riepilogato nei passaggi seguenti:

1.  Quando si carica un profilo che deve essere utilizzato dal writer, l'oggetto writer assegna un numero di input per ogni connessione nel profilo. Per ulteriori informazioni sul caricamento dei profili per il writer, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md). A meno che non si usi l'esclusione reciproca per velocità in bit, esiste una connessione per ogni flusso. I flussi che si escludono a vicenda dalla velocità in bit condividono una singola connessione.
2.  L'applicazione deve identificare i numeri di input per il file. Per ulteriori informazioni sull'identificazione dei numeri di input, vedere [per identificare gli input per numero](to-identify-inputs-by-number.md).
3.  Per ogni input, è necessario assicurarsi che il formato di input corrisponda ai dati. È possibile enumerare i formati di input supportati dall'SDK. Per ulteriori informazioni, vedere [per enumerare i formati di input](to-enumerate-input-formats.md). Non è possibile enumerare i formati di input di flussi arbitrari o flussi già compressi. Per ulteriori informazioni su questi casi speciali, vedere [input di flusso arbitrario e precompresso](arbitrary-and-precompressed-stream-inputs.md).
4.  Assegnare il formato di input corretto per ogni connessione. Per ulteriori informazioni, vedere [assegnazione dei formati di input](assigning-input-formats.md).
5.  Alcune funzionalità di codec e writer sono configurate in fase di codifica anziché nel profilo. Per configurare queste funzionalità, è necessario utilizzare le impostazioni di input. Per ulteriori informazioni, vedere [per impostare le impostazioni di input](to-set-input-settings.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




