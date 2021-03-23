---
title: Firme radice
description: La firma radice definisce i tipi di risorse associati alla pipeline grafica.
ms.assetid: ee32a222-8469-4af5-b688-afa70cf77c6a
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4c034e208dd841545777cc92878e7020b9b4a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548845"
---
# <a name="root-signatures"></a>Firme radice

La firma radice definisce i tipi di risorse associati alla pipeline grafica.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cenni preliminari sulle firme radice](root-signatures-overview.md)<br/>                                                 | Una firma radice viene configurata tramite l'app e collega gli elenchi di comandi alle risorse necessarie per gli shader. L'elenco dei comandi di grafica include una firma della radice di calcolo e grafica. Un elenco di comandi di calcolo avrà semplicemente una firma radice di calcolo. Queste firme radice sono indipendenti l'una dall'altra.<br/>                                                                                             |
| [Uso di una firma radice](using-a-root-signature.md)<br/>                                                     | La firma radice è la definizione di una raccolta disposta in modo arbitrario di tabelle dei descrittori (incluso il relativo layout), costanti radice e descrittori radice. Ogni voce ha un costo verso un limite massimo, pertanto l'applicazione può comportare un compromesso tra il numero di ogni tipo di voce che la firma radice conterrà.<br/>                                                                     |
| [Creazione di una firma radice](creating-a-root-signature.md)<br/>                                               | Le firme radice sono una struttura di dati complessa contenente strutture annidate. Questi possono essere definiti a livello di codice usando la definizione della struttura di dati riportata di seguito, che include i metodi per inizializzare i membri. In alternativa, possono essere creati in HLSL (High Level Shading Language) offrendo il vantaggio che il compilatore convaliderà prima che il layout sia compatibile con lo shader. <br/> |
| [Limiti della firma radice](root-signature-limits.md)<br/>                                                       | La firma radice è una proprietà di primo livello e sono previsti limiti e costi severi da considerare.<br/>                                                                                                                                                                                                                                                                                                            |
| [Uso di costanti direttamente nella firma radice](using-constants-directly-in-the-root-signature.md)<br/>     | Le applicazioni possono definire costanti radice nella firma radice, ognuna come un set di valori a 32 bit. Vengono visualizzati in HLSL (High Level Shading Language) come buffer costante. Si noti che i buffer costanti per motivi cronologici vengono visualizzati come set di valori a 4x32 bit. <br/>                                                                                                                                        |
| [Uso dei descrittori direttamente nella firma radice](using-descriptors-directly-in-the-root-signature.md)<br/> | Le applicazioni possono inserire descrittori direttamente nella firma radice per evitare di dover passare attraverso un heap del descrittore. Questi descrittori hanno una grande quantità di spazio nella firma radice (vedere la sezione limiti della firma radice), per cui le applicazioni devono utilizzarle sporadicamente. <br/>                                                                                                                                     |
| [Firme radice di esempio](example-root-signatures.md)<br/>                                                   | Nella sezione seguente vengono illustrate le firme radice che variano in complessità da vuote a completamente complete.<br/>                                                                                                                                                                                                                                                                                                       |
| [Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)<br/>                             | La specifica delle firme radice nel modello HLSL shader 5,1 rappresenta un'alternativa alla relativa specifica nel codice C++.<br/>                                                                                                                                                                                                                                                                                                  |
| [Firma radice versione 1,1](root-signature-version-1-1.md)<br/>                                             | Lo scopo della firma radice versione 1,1 è quello di consentire alle applicazioni di indicare ai driver quando i descrittori in un heap del descrittore hanno vinto la modifica o i descrittori di dati puntano a won t. Ciò consente all'opzione per i driver di eseguire ottimizzazioni che potrebbero essere possibili sapendo che un descrittore o la memoria a cui fa riferimento è statico per un determinato periodo di tempo. <br/>                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)
</dt> <dt>

[**ID3D12RootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

