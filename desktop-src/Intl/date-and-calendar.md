---
description: A ogni impostazione locale è associato un tipo di calendario predefinito (tipo di dati CALTYPE). Le impostazioni locali possono anche avere un tipo di calendario alternativo. Per informazioni dettagliate sui tipi di calendario, vedere Informazioni sul tipo di calendario.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Data e calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f200ccd60a5a5d121a8774c01808794e744b98d8611210fcc98b0f8e5e1f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822811"
---
# <a name="date-and-calendar"></a>Data e calendario

A [ogni impostazione](locales-and-languages.md) locale è associato un tipo di calendario predefinito (tipo di dati CALTYPE). Le impostazioni locali possono anche avere un tipo di calendario alternativo. Per informazioni dettagliate sui tipi di calendario, vedere [Informazioni sul tipo di calendario](calendar-type-information.md).

> [!Note]  
> Per usare un tipo di calendario alternativo per le impostazioni locali, l'applicazione deve impostare la costante [ \_ LOCALE IOPTIONALCALENDAR](locale-ioptionalcalendar.md) sul tipo di calendario alternativo per le impostazioni locali.

 

La maggior parte delle impostazioni locali usa il calendario gregoriano standard e un numero impostato di formati di data. Queste opzioni predefinite per i formati di data sono disponibili per la visualizzazione tramite la [**funzione EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) o [**EnumDateFormatsEx.**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)

Alcune impostazioni locali richiedono considerazioni speciali quando si crea un elenco completo di opzioni di formato. Alcune di queste impostazioni locali richiedono l'inserimento di stringhe di testo nella stringa di formato della data, mentre altre richiedono un metodo di calcolo dei valori completamente diverso. Un'applicazione risolve questi requisiti speciali con l'aggiunta di determinati tipi di informazioni sulle impostazioni locali e tipi di calendario.

Per informazioni dettagliate sull'implementazione di date e calendari nelle applicazioni, vedere Recupero di informazioni su [data e ora](retrieving-time-and-date-information.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Informazioni sul tipo di calendario](calendar-type-information.md)
</dt> <dt>

[Recupero di informazioni su ora e data](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



