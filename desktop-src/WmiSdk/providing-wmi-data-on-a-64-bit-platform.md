---
description: Gli script e le applicazioni scritti per i sistemi operativi a 32 bit dovrebbero continuare a funzionare correttamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fornire dati WMI in una piattaforma a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527745"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Fornire dati WMI in una piattaforma a 64 bit

Gli script e le applicazioni scritti per i sistemi operativi a 32 bit dovrebbero continuare a funzionare correttamente. Se è presente un provider a 32 bit, è possibile valutare se è necessario scrivere una versione a 64 bit per l'operazione side-by-side. In genere, entrambe le versioni non sono necessarie e la versione a 64 bit può servire sia il client locale che quello remoto a 32 bit e 64 bit. Tuttavia, per la modalità di compatibilità delle applicazioni a 32 bit, utilizzare il provider WMI esistente a 32 bit in un sistema a 64 bit eseguito in modalità WOW64 a 32 bit.

In rari casi, sia i provider a 32 bit che quelli a 64 bit devono essere eseguiti side-by-side nei sistemi a 64 bit. In questo caso, la versione appropriata del provider che viene caricata varia a seconda che il chiamante sia a 32 bit o a 64 bit e locale o remoto. Un chiamante che utilizza i flag di contesto dell'oggetto connessione, **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture**, può richiedere che WMI carichi un provider non predefinito. Per altre informazioni, vedere [ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md).

Nel caso insolito in cui è necessario eseguire i provider a 32 bit e a 64 bit side-by-Side, è necessario assicurarsi che gli scenari di installazione e disinstallazione vengano gestiti con cautela. Poiché WMI dispone solo di un [*repository*](gloss-w.md) e le versioni a 32 bit e 64 bit di [**mofcomp.exe**](mofcomp.md) inserire i dati nello stesso repository. non esiste alcuna distinzione tra un file con estensione MOF a 32 bit o a 64 bit. La reinstallazione di una versione del provider non è danneggiata: verranno compilati i file con estensione MOF e le classi archiviate nel repository. Tuttavia, una seconda disinstallazione che elimina uno spazio dei nomi può interferire con il funzionamento dell'altro provider.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottenere e fornire dati in un computer a 64 bit](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Richiesta di dati WMI in una piattaforma a 64 bit](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Invio di dati a WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



