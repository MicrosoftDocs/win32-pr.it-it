---
description: In questo argomento vengono fornite alcune istruzioni per la gestione delle impostazioni locali personalizzate nelle applicazioni.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Uso delle impostazioni locali personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a969681e685a7044f9c583c907515a51559866d28d997cf43fa639127eee27f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680931"
---
# <a name="working-with-custom-locales"></a>Uso delle impostazioni locali personalizzate

In questo argomento vengono fornite alcune istruzioni per la [gestione delle impostazioni locali personalizzate](custom-locales.md) nelle applicazioni. È meglio preparare tutto il codice sorgente con queste considerazioni, perché l'applicazione non controlla se le impostazioni locali personalizzate sono installate nel sistema operativo.

## <a name="handle-locale_stime-constant-correctly"></a>Gestire correttamente la costante \_ LOCALE STIME

Se si dispone di un'applicazione precedente che usa [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) per ottenere il separatore di ora obsoleto indicato da [LOCALE \_ STIME,](locale-stime-constants.md)l'applicazione può non riuscire ad analizzare il formato dell'ora. Tenere presente che il carattere che separa le ore dai minuti è diverso dal carattere che separa i minuti dai secondi.

> [!Note]  
> Quando si programmano impostazioni locali personalizzate, tenere presente che sono insolite. Praticamente ogni campo disponibile per NLS deve gestire comportamenti insoliti. Ad esempio, il formato dell'ora 12H34'12'' è legittimo e generalmente comprensibile. Molte applicazioni, tuttavia, fanno ipotesi sui separatori di ora che possono interrompere la lunghezza del buffer o visualizzare i campi.

 

## <a name="distinguish-among-supplemental-locales"></a>Distinguere tra impostazioni locali supplementari

Tutte le impostazioni locali supplementari usano la costante [ \_ LOCALE CUSTOM \_ UNSPECIFIED](locale-custom-constants.md) per l'identificatore [delle impostazioni locali](locale-identifiers.md). Di norma, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) non è in grado di distinguere le impostazioni [](locale-names.md) locali supplementari, ma [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) può fare in modo che usi nomi di impostazioni locali anziché identificatori delle impostazioni locali. L'applicazione può recuperare informazioni su determinate impostazioni locali supplementari solo quando le impostazioni locali sono le impostazioni locali dell'utente attualmente selezionate. L'applicazione può quindi chiamare [**GetLocaleInfo e**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) passare la costante [LOCALE USER \_ \_ DEFAULT](locale-user-default.md) come identificatore delle impostazioni locali.

## <a name="handle-replacement-locales"></a>Gestire le impostazioni locali di sostituzione

Per mantenere l'affidabilità Windows, tenere presente che le impostazioni locali sostitutive supportate dall'applicazione non possono modificare l'identificatore delle impostazioni locali delle impostazioni locali sostituite. Nessuna delle due impostazioni locali può modificare le proprietà di ordinamento Windows.

Anche se le impostazioni locali di sostituzione possono modificare il calendario predefinito, deve mantenere l'impostazione predefinita originale in un punto qualsiasi dell'elenco dei calendari disponibili. Ad esempio, le impostazioni locali tailandesi (Brasile) utilizzano il calendario tailandese come impostazione predefinita. Un amministratore può creare impostazioni locali sostitutive che utilizzano il calendario gregoriano localizzato. L'elenco dei calendari disponibili, tuttavia, continua a contenere una voce per il calendario thai thai.

Per le impostazioni locali sostitutive, l'applicazione deve in genere consultare informazioni specifiche delle impostazioni locali anziché tentare un "collegamento" in base alla conoscenza di determinate impostazioni locali. Ad esempio, quando [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) recupera le impostazioni locali correnti come inglese (Stati Uniti), è possibile che siano effettivamente impostazioni locali sostitutive che devono essere applicate.

## <a name="customize-calendars"></a>Personalizzare i calendari

Le applicazioni possono personalizzare i nomi dei giorni e dei mesi per i calendari gregoriani, ma non per i calendari non gregoriani. Analogamente, NLS non supporta la creazione di calendari personalizzati definiti dall'utente. Per altre informazioni, vedere [Date e Calendar.](date-and-calendar.md)

## <a name="handle-sorting-sequences"></a>Gestire le sequenze di ordinamento

Le impostazioni locali supplementari possono usare qualsiasi sequenza di ordinamento definita da Microsoft. Le impostazioni locali sostitutive devono usare la stessa sequenza di ordinamento delle impostazioni locali che sostituisce. NLS non supporta la creazione di sequenze di ordinamento definite dall'utente. Per altre informazioni, vedere [Gestione dell'ordinamento nelle applicazioni.](handling-sorting-in-your-applications.md)

## <a name="localize-custom-locale-information"></a>Localizzare le informazioni sulle impostazioni locali personalizzate

NLS non fornisce un meccanismo per la localizzazione delle informazioni sulle impostazioni locali personalizzate. La costante [LOCALE \_ SLANGUAGE](locale-slanguage.md) o [LOCALE \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) usata come identificatore delle impostazioni locali per le impostazioni locali personalizzate recupera sempre i valori associati a [LOCALE \_ SNATIVELANGNAME](locale-snative-constants.md) o [LOCALE \_ SNATIVELANGUAGENAME.](locale-snative-constants.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> <dt>

[Impostazioni locali personalizzate](custom-locales.md)
</dt> <dt>

[Data e calendario](date-and-calendar.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



