---
description: In questo argomento vengono fornite alcune istruzioni per la gestione delle impostazioni locali personalizzate nelle applicazioni.
ms.assetid: 2622e2b3-b952-4666-a440-85d73d11c5e0
title: Utilizzo di impostazioni locali personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab0e59446496ae2985860c0fd6b1bd5bddde084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966974"
---
# <a name="working-with-custom-locales"></a>Utilizzo di impostazioni locali personalizzate

In questo argomento vengono fornite alcune istruzioni per la gestione delle [impostazioni locali personalizzate](custom-locales.md) nelle applicazioni. È preferibile preparare tutto il codice sorgente tenendo presente queste considerazioni, in quanto l'applicazione non controlla se le impostazioni locali personalizzate sono installate nel sistema operativo.

## <a name="handle-locale_stime-constant-correctly"></a>Gestire correttamente la \_ costante stime delle impostazioni locali

Se si dispone di un'applicazione precedente che usa [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) per ottenere il separatore dell'ora obsoleto indicato dalle [impostazioni locali \_ stime](locale-stime-constants.md), l'applicazione potrebbe non riuscire ad analizzare il formato dell'ora. Tenere presente che il carattere che separa le ore dai minuti è diverso dal carattere che separa i minuti dai secondi.

> [!Note]  
> Quando si programmano impostazioni locali personalizzate, tenere presente che sono insolite. Praticamente ogni campo disponibile per NLS deve far fronte a un comportamento insolito. Il formato dell'ora 12H34 '12 '', ad esempio, è legittimo e generalmente comprensibile. Tuttavia, molte applicazioni fanno supposizioni sui separatori temporali che possono interrompere le lunghezze del buffer o visualizzare i campi.

 

## <a name="distinguish-among-supplemental-locales"></a>Distinguere tra impostazioni locali aggiuntive

Tutte le impostazioni locali aggiuntive utilizzano la costante non [ \_ \_ specificata locale personalizzata](locale-custom-constants.md) per l'identificatore delle [impostazioni locali](locale-identifiers.md). Di norma, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) non è in grado di distinguere tra le impostazioni locali supplementari, ma [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) può usare [i nomi delle impostazioni locali](locale-names.md) anziché gli identificatori delle impostazioni locali. L'applicazione può recuperare le informazioni relative a determinate impostazioni locali aggiuntive solo quando queste impostazioni locali sono le impostazioni locali dell'utente correntemente selezionate. L'applicazione può quindi chiamare [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e passare il [ \_ \_ valore predefinito dell'utente delle impostazioni locali](locale-user-default.md) costante come identificatore delle impostazioni locali.

## <a name="handle-replacement-locales"></a>Gestisci impostazioni locali sostitutive

Per mantenere l'affidabilità di Windows, tenere presente che le impostazioni locali sostitutive supportate dall'applicazione non possono modificare l'identificatore delle impostazioni locali sostituite. Nessuna delle impostazioni locali sostitutive consente di modificare le proprietà di ordinamento di Windows.

Sebbene le impostazioni locali sostitutive possano modificare il calendario predefinito, è necessario mantenere il valore predefinito originale in un punto qualsiasi dell'elenco dei calendari disponibili. Ad esempio, le impostazioni locali Thai (Tailandia) usano il calendario buddista tailandese come valore predefinito. Un amministratore può creare le impostazioni locali sostitutive che usano il calendario localizzato gregoriano. Tuttavia, l'elenco dei calendari disponibili continua a contenere una voce per il calendario buddista tailandese.

Per le impostazioni locali sostitutive, l'applicazione in genere deve consultare le informazioni specifiche delle impostazioni locali anziché tentare un "collegamento" in base alla conoscenza di determinate impostazioni locali. Ad esempio, quando [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) recupera le impostazioni locali correnti come inglese (Stati Uniti), potrebbe essere effettivamente un'impostazione locale sostitutiva che dovrebbe avere effetto.

## <a name="customize-calendars"></a>Personalizzare i calendari

Le applicazioni possono personalizzare i nomi dei giorni e dei mesi per i calendari gregoriani, ma non per i calendari non gregoriani. Analogamente, NLS non supporta la creazione di calendari personalizzati definiti dall'utente. Per ulteriori informazioni, vedere [data e calendario](date-and-calendar.md).

## <a name="handle-sorting-sequences"></a>Gestisci sequenze di ordinamento

Le impostazioni locali aggiuntive possono usare qualsiasi sequenza di ordinamento definita da Microsoft. Le impostazioni locali di sostituzione devono usare la stessa sequenza di ordinamento delle impostazioni locali che sostituisce. NLS non supporta la creazione di sequenze di ordinamento definite dall'utente. Per ulteriori informazioni, vedere [gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).

## <a name="localize-custom-locale-information"></a>Localizzare le informazioni sulle impostazioni locali personalizzate

NLS non fornisce un meccanismo per localizzare le informazioni sulle impostazioni locali personalizzate. In questo modo, le impostazioni locali costanti [ \_ SLANGUAGE](locale-slanguage.md) o [ \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md) delle impostazioni locali usate come identificatore delle impostazioni locali per le impostazioni locali personalizzate recuperano sempre i valori associati alle impostazioni [locali \_ SNATIVELANGNAME](locale-snative-constants.md) o le [impostazioni locali \_ SNATIVELANGUAGENAME](locale-snative-constants.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Impostazioni locali personalizzate](custom-locales.md)
</dt> <dt>

[Data e calendario](date-and-calendar.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> </dl>

 

 



