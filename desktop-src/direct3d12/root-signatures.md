---
title: Firme radice
description: La firma radice definisce quali tipi di risorse sono associati alla pipeline grafica.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867e5bfb1f77a8f70c97b4a62efc3ed63e2d780c83eb0a844193a24f5ed3f87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912235"
---
# <a name="root-signatures"></a>Firme radice

La firma radice definisce quali tipi di risorse sono associati alla pipeline grafica.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Panoramica delle firme radice](root-signatures-overview.md)<br/>                                                 | Una firma radice viene configurata dall'app e collega gli elenchi di comandi alle risorse richieste dagli shader. L'elenco dei comandi di grafica ha sia una firma radice grafica che una firma radice di calcolo. Un elenco di comandi di calcolo avrà semplicemente una firma radice di calcolo. Queste firme radice sono indipendenti l'una dall'altra.<br/>                                                                                             |
| [Uso di una firma radice](using-a-root-signature.md)<br/>                                                     | La firma radice è la definizione di una raccolta arbitrariamente di tabelle descrittori (incluso il layout), costanti radice e descrittori radice. Ogni voce ha un costo per un limite massimo, quindi l'applicazione può bilanciare il saldo tra il numero di ogni tipo di voce che la firma radice conterrà.<br/>                                                                     |
| [Creazione di una firma radice](creating-a-root-signature.md)<br/>                                               | Le firme radice sono una struttura di dati complessa contenente strutture annidate. Questi elementi possono essere definiti a livello di codice usando la definizione della struttura dei dati riportata di seguito , che include metodi che consentono di inizializzare i membri. In alternativa, possono essere creati in HLSL (High Level Shading Language) offrendo il vantaggio che il compilatore convaliderà in anticipo che il layout è compatibile con lo shader. <br/> |
| [Limiti della firma radice](root-signature-limits.md)<br/>                                                       | La firma radice è un'importante proprietà immobiliare e sono previsti limiti e costi rigorosi da considerare.<br/>                                                                                                                                                                                                                                                                                                            |
| [Uso di costanti direttamente nella firma radice](using-constants-directly-in-the-root-signature.md)<br/>     | Le applicazioni possono definire costanti radice nella firma radice, ognuna come set di valori a 32 bit. Vengono visualizzati in HLSL (High Level Shading Language) come buffer costante. Si noti che i buffer costanti per motivi cronologici vengono visualizzati come set di valori a 4x32 bit. <br/>                                                                                                                                        |
| [Uso dei descrittori direttamente nella firma radice](using-descriptors-directly-in-the-root-signature.md)<br/> | Le applicazioni possono inserire i descrittori direttamente nella firma radice per evitare di dover passare attraverso un heap dei descrittori. Questi descrittori prendono molto spazio nella firma radice (vedere la sezione limiti della firma radice), quindi le applicazioni devono usarli con parsimonio. <br/>                                                                                                                                     |
| [Firme radice di esempio](example-root-signatures.md)<br/>                                                   | La sezione seguente illustra le firme radice che variano in complessità da vuota a completa.<br/>                                                                                                                                                                                                                                                                                                       |
| [Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | Specificare le firme radice in HLSL Shader Model 5.1 è un'alternativa a specificarle nel codice C++.<br/>                                                                                                                                                                                                                                                                                                  |
| [Firma radice versione 1.1](root-signature-version-1-1.md)<br/>                                             | Lo scopo della versione 1.1 della firma radice è consentire alle applicazioni di indicare ai driver quando i descrittori in un heap dei descrittori non cambiano o i descrittori di dati puntano a non cambiano. Ciò consente ai driver di eseguire ottimizzazioni che potrebbero essere possibili sapendo che un descrittore o la memoria a cui punta è statico per un certo periodo di tempo. <br/>                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

