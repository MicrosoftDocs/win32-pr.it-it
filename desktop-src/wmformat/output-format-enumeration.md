---
title: Enumerazione del formato di output
description: Enumerazione del formato di output
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK, enumerazioni del formato di output
- Advanced Systems Format (ASF), enumerazioni del formato di output
- ASF (formato avanzato dei sistemi), enumerazioni del formato di output
- Windows Media Format SDK, interfaccia IWMReaderTypeNegotiation
- Advanced Systems Format (ASF), interfaccia IWMReaderTypeNegotiation
- ASF (formato avanzato dei sistemi), interfaccia IWMReaderTypeNegotiation
- enumerazioni del formato di output
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046262"
---
# <a name="output-format-enumeration"></a>Enumerazione del formato di output

Sia l'oggetto Reader che l'oggetto Reader sincrono comunicano con i codec per enumerare i formati di output possibili per i flussi compressi. Quando si legge un file contenente contenuti compressi con uno o più codec Windows Media, è possibile esaminare i possibili formati di output per scegliere quello più adatto alle proprie esigenze. Per praticità, ogni codec ha un formato di output predefinito impostato sul formato usato più di frequente. Per ulteriori informazioni sull'enumerazione di output, vedere [utilizzo degli output](working-with-outputs.md).

È possibile apportare alcune modifiche a un formato di output a seconda del tipo di supporto. Per i flussi video, ad esempio, è possibile modificare le dimensioni del frame e la profondità del colore. Gli oggetti di lettura supportano entrambi un'interfaccia per testare le modifiche apportate al formato di output, denominato [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di lettura file**](file-reading-features.md)
</dt> </dl>

 

 




