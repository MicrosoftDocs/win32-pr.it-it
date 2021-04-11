---
title: Esempi di supporto (Windows Media Format 11 SDK)
description: Esempi di supporti
ms.assetid: 5fe0d261-c4a8-4b8e-b5dd-668ce067723c
keywords:
- Windows Media Format SDK, esempi di supporti
- Windows Media Format SDK, esempi
- Advanced Systems Format (ASF), esempi di supporti
- ASF (Advanced Systems Format), esempi di supporti
- ASF (Advanced Systems Format), esempi
- ASF (formato avanzato dei sistemi), esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d46a933775877f4566115ba3936c0f9f8bd7b3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963702"
---
# <a name="media-samples-windows-media-format-11-sdk"></a>Esempi di supporto (Windows Media Format 11 SDK)

Un esempio multimediale, o esempio, è un blocco di dati multimediali digitali. Un esempio è l'unità di base che viene modificata dagli oggetti di lettura e scrittura di Windows Media Format SDK. Il contenuto di un singolo campione è determinato dal tipo di supporto associato all'esempio. Per video, ogni esempio rappresenta un singolo frame. Per l'audio, la quantità di dati in un singolo campione viene impostata nel profilo utilizzato per creare il file ASF.

Gli esempi possono contenere dati non compressi oppure possono contenere dati compressi, nel qual caso vengono chiamati esempi di *flusso*. Quando si crea un file ASF, gli esempi vengono passati al writer. Il writer coordina la compressione degli esempi con il codec appropriato e dispone i dati compressi nella sezione dati del file ASF. Durante la riproduzione, il lettore legge i dati compressi, li decomprime e fornisce i dati non compressi ricostruiti come esempi di output.

Tutti gli esempi usati da Windows Media Format SDK vengono incapsulati in un oggetto buffer la cui memoria viene allocata automaticamente dai componenti di runtime dell'SDK. Se necessario, è anche possibile allocare i propri buffer, usando le funzionalità avanzate del writer e del lettore.

**Nota** Il termine esempio viene usato in questo SDK per fare riferimento a un esempio di supporto, non a un esempio di audio. Nella codifica audio un esempio si riferisce a un singolo valore audio codificato. In genere, la qualità dell'audio codificato viene specificata da un numero di campioni al secondo. Ad esempio, il suono di qualità CD viene registrato a 44.100 campioni al secondo. Questo valore viene comunemente abbreviato con la notazione Hz, quindi 44.100 campioni al secondo saranno 44.100 Hz o 44,1 kHz.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Concetti**](concepts.md)
</dt> <dt>

[**Interfaccia INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Input, flussi e output**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




