---
description: Le applicazioni client e gli script che accedono ai provider WMI a 32 bit standard continuano a funzionare normalmente quando vengono eseguiti in un sistema operativo a 64 bit.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Recupero e fornitura di dati in un computer a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46163290d1212fd66bef48dba177034769360e8d7c6249dfdf40327ce2adc32c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819380"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a>Recupero e fornitura di dati in un computer a 64 bit

Le applicazioni client e gli script che accedono ai provider WMI a 32 bit standard continuano a funzionare normalmente quando vengono eseguiti in un sistema operativo a 64 bit. Solo due provider preinstallati, il [provider](/previous-versions/windows/desktop/regprov/system-registry-provider) del Registro di sistema e il [provider View,](view-provider.md)hanno versioni a 64 bit che vengono eseguite side-by-side con le versioni a 32 bit. Tuttavia, un'applicazione a 32 bit che richiede istanze di Windows Driver Model (WDM) a 32 bit riceve le istanze della classe WDM a 64 bit predefinite in un sistema operativo a 64 bit.

## <a name="accessing-default-and-nondefault-provider-data"></a>Accesso ai dati predefiniti e non predefiniti del provider

In genere, i writer di provider non includono versioni a 32 bit e a 64 bit di un provider nello stesso sistema operativo. Se non esiste alcun provider a 64 bit, un provider a 32 bit può continuare a essere eseguito tramite le funzionalità di WOW64. Analogamente, un provider a 64 bit può fornire dati a un'applicazione a 32 bit. Per altre informazioni, vedere [Specifica di dati WMI in una piattaforma a 64 bit.](providing-wmi-data-on-a-64-bit-platform.md)

Se esistono due versioni, le applicazioni client e gli script possono usare i parametri di contesto disponibili [nell'API COM](com-api-for-wmi.md) e nell'API [di](scripting-api-for-wmi.md) scripting per connettersi in modo esplicito a un provider WMI non predefinito specifico, se disponibile. Per altre informazioni, vedere [Richiesta di dati WMI in una piattaforma a 64 bit.](requesting-wmi-data-on-a-64-bit-platform.md)

Il diagramma seguente illustra le connessioni predefinite e non predefinite, usando il Registro di sistema come esempio per cui due provider possono esistere side-by-side in una piattaforma a 64 bit.

![connessioni predefinite e non predefinite su una piattaforma a 64 bit](images/32-64bit-registry.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiesta di dati WMI su una piattaforma a 64 bit](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fornire dati WMI in una piattaforma a 64 bit](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
