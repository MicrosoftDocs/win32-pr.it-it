---
description: Le applicazioni e gli script client che accedono a provider WMI 32 bit standard continuano a funzionare normalmente in caso di esecuzione in un sistema operativo a 64 bit.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Ottenere e fornire dati in un computer a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555815"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Ottenere e fornire dati in un computer a 64 bit

Le applicazioni e gli script client che accedono a provider WMI 32 bit standard continuano a funzionare normalmente in caso di esecuzione in un sistema operativo a 64 bit. Solo due provider preinstallati, il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) e il [provider di visualizzazione](view-provider.md), hanno versioni a 64 bit che vengono eseguite side-by-side con le versioni a 32 bit. Tuttavia, un'applicazione a 32 bit che richiede istanze di Windows Driver Model WDM (32 bit) riceve le istanze della classe WDM a 64 bit predefinite in un sistema operativo a 64 bit.

## <a name="accessing-default-and-nondefault-provider-data"></a>Accesso ai dati del provider predefiniti e non predefiniti

In genere, i writer del provider non includono le versioni a 32 bit e a 64 bit di un provider nello stesso sistema operativo. Se non esiste alcun provider a 64 bit, un provider a 32 bit può continuare a eseguire le funzionalità di WOW64. Un provider a 64 bit può fornire dati in modo analogo a un'applicazione a 32 bit. Per ulteriori informazioni, vedere [la pagina relativa alla fornitura di dati WMI in una piattaforma a 64 bit](providing-wmi-data-on-a-64-bit-platform.md).

Se esistono due versioni, le applicazioni e gli script client possono usare i parametri di contesto disponibili nell' [API com](com-api-for-wmi.md) e l' [API di scripting](scripting-api-for-wmi.md) per connettersi in modo esplicito a un provider WMI non predefinito specifico, se disponibile. Per ulteriori informazioni, vedere la pagina relativa alla [richiesta di dati WMI in una piattaforma a 64 bit](requesting-wmi-data-on-a-64-bit-platform.md).

Il diagramma seguente illustra le connessioni predefinite e non predefinite, usando il registro di sistema come esempio per cui due provider possono esistere side-by-side in una piattaforma a 64 bit.

![connessioni predefinite e non predefinite in una piattaforma a 64 bit](images/32-64bit-registry.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta di dati WMI in una piattaforma a 64 bit](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fornire dati WMI in una piattaforma a 64 bit](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
