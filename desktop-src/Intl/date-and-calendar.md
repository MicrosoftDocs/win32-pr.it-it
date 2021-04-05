---
description: A ogni impostazioni locali è associato un tipo di calendario predefinito (tipo di dati CALTYPE). Le impostazioni locali possono anche avere un tipo di calendario alternativo. Per informazioni dettagliate sui tipi di calendario, vedere informazioni sul tipo di calendario.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Data e calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884581"
---
# <a name="date-and-calendar"></a>Data e calendario

A ogni [impostazioni locali](locales-and-languages.md) è associato un tipo di calendario predefinito (tipo di dati CALTYPE). Le impostazioni locali possono anche avere un tipo di calendario alternativo. Per informazioni dettagliate sui tipi di calendario, vedere [informazioni sul tipo di calendario](calendar-type-information.md).

> [!Note]  
> Per usare un tipo di calendario alternativo per le impostazioni locali, l'applicazione deve impostare la costante [ \_ IOPTIONALCALENDAR delle impostazioni locali](locale-ioptionalcalendar.md) sul tipo di calendario alternativo per le impostazioni locali.

 

La maggior parte delle impostazioni locali utilizza il calendario gregoriano standard e un numero impostato di formati di data. Queste opzioni predefinite per i formati di data sono disponibili per la visualizzazione tramite la funzione [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) o [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .

Alcune impostazioni locali richiedono considerazioni speciali quando si crea un elenco completo di opzioni di formattazione. Per alcune di queste impostazioni locali è necessario inserire stringhe di testo nella stringa di formato della data, mentre altre richiedono un metodo di calcolo dei valori completamente diverso. Un'applicazione soddisfa questi requisiti speciali mediante l'aggiunta di determinati tipi di informazioni sulle impostazioni locali e tipi di calendario.

Per informazioni dettagliate sull'implementazione di date e calendari nelle applicazioni, vedere [recupero di informazioni su data e ora](retrieving-time-and-date-information.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Informazioni sul tipo di calendario](calendar-type-information.md)
</dt> <dt>

[Recupero di informazioni su data e ora](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



