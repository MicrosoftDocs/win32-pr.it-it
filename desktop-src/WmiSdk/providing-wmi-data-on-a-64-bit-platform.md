---
description: Gli script e le applicazioni scritti per i sistemi operativi a 32 bit devono continuare a funzionare correttamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fornire dati WMI in una piattaforma a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cb8a7e698723c6d4705a735591097fe7cf354db9684924d58f6b363c0ae6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992641"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Fornire dati WMI in una piattaforma a 64 bit

Gli script e le applicazioni scritti per i sistemi operativi a 32 bit devono continuare a funzionare correttamente. Se si dispone di un provider a 32 bit esistente, è possibile valutare se è necessario scrivere una versione a 64 bit per l'operazione side-by-side. In genere, entrambe le versioni non sono necessarie e la versione a 64 bit può essere utilizzata per client locali o remoti a 32 bit e a 64 bit. Tuttavia, per la modalità di compatibilità delle applicazioni a 32 bit, usare il provider WMI a 32 bit esistente in un sistema a 64 bit eseguito in modalità WOW64 a 32 bit.

In rare situazioni, i provider a 32 bit e a 64 bit devono essere eseguiti side-by-side in sistemi a 64 bit. In questo caso, la versione appropriata del provider caricata dipende dal fatto che il chiamante sia a 32 bit o a 64 bit e locale o remoto. Un chiamante che usa i flag di contesto dell'oggetto **\_ \_ connessione, ProviderArchitecture** e **\_ \_ RequiredArchitecture,** può richiedere a WMI di caricare un provider non predefinito. Per altre informazioni, vedere [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).

Nel caso insolito in cui sia necessario eseguire i provider a 32 bit e a 64 bit side-by-side, è necessario assicurarsi che gli scenari di installazione e disinstallazione siano gestiti con attenzione. Questo perché WMI ha un solo [*repository*](gloss-w.md) e le versioni a 32 bit e a 64 bit di [**mofcomp.exe**](mofcomp.md) inserire i dati nello stesso repository; non esiste alcuna distinzione tra un file MOF a 32 bit o a 64 bit. La reinstallazione di una versione del provider non intaserà: i file mof verranno compilati e le classi archiviate nel repository. Tuttavia, una seconda disinstallazione che elimina uno spazio dei nomi può interferire con il funzionamento dell'altro provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero e fornitura di dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Richiesta di dati WMI su una piattaforma a 64 bit](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fornire dati a WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



