---
title: Enumerazione del formato di output
description: Enumerazione del formato di output
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK, enumerazioni del formato di output
- Advanced Systems Format (ASF), enumerazioni del formato di output
- ASF (Advanced Systems Format), enumerazioni del formato di output
- Windows Media Format SDK, interfaccia IWMReaderTypeNegotiation
- Advanced Systems Format (ASF), interfaccia IWMReaderTypeNegotiation
- ASF (Advanced Systems Format), interfaccia IWMReaderTypeNegotiation
- Enumerazioni del formato di output
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd1e6dacf4daac3f8c5f74fa1b4d9dd83c5cb3be538dc983b671a9f9096325f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027359"
---
# <a name="output-format-enumeration"></a>Enumerazione del formato di output

Sia l'oggetto lettore che l'oggetto lettore sincrono comunicano con i codec per enumerare i possibili formati di output per i flussi compressi. Quando si legge un file contenente contenuto compresso con uno o più codec Windows Media, è possibile esaminare i possibili formati di output per scegliere quello più adatto alle proprie esigenze. Per praticità, ogni codec ha un formato di output predefinito impostato sul formato usato più comunemente. Per altre informazioni sull'enumerazione di output, vedere [Utilizzo degli output](working-with-outputs.md).

È possibile apportare determinate modifiche a un formato di output a seconda del tipo di supporto. Per i flussi video, ad esempio, è possibile modificare le dimensioni dei fotogrammi e la profondità del colore. Entrambi gli oggetti di lettura supportano un'interfaccia per testare le modifiche apportate al formato di output, denominato [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di lettura file**](file-reading-features.md)
</dt> </dl>

 

 




