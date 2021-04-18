---
description: Recupero e impostazione delle informazioni sulle impostazioni locali
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recupero e impostazione delle informazioni sulle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f9faa8749073016862587330776f32e65749b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306603"
---
# <a name="retrieving-and-setting-locale-information"></a>Recupero e impostazione delle informazioni sulle impostazioni locali

L'applicazione deve essere in grado di recuperare e impostare informazioni specifiche sulle [impostazioni locali e le lingue](locales-and-languages.md)disponibili. Ogni elemento delle informazioni sulle impostazioni locali, ad esempio il nome di un particolare giorno della settimana o il carattere usato come separatore decimale, presenta una costante corrispondente. Le costanti disponibili sono definite in [costanti di informazioni sulle impostazioni locali](locale-information-constants.md).

L'applicazione archivia e modifica sempre le informazioni sulle impostazioni locali come una stringa con terminazione null. Non sono consentiti dati binari e tutti i valori numerici devono essere specificati come testo. Ogni tipo di informazioni ha un formato particolare. Inoltre, diversi tipi sono collegati tra loro in modo che la modifica di un tipo modifichi anche il valore dell'altro tipo.

Per recuperare le informazioni sulle impostazioni locali, l'applicazione chiama [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante che corrisponde alle informazioni richieste. L'applicazione può chiamare [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) per impostare un elemento delle informazioni sulle impostazioni locali.

> [!Note]  
> Sebbene sia possibile supportare un [identificatore delle impostazioni locali](locale-identifiers.md) , non è disponibile per l'utilizzo da parte di un'applicazione a meno che non vengano installate anche le impostazioni locali corrispondenti.

 

Poiché la maggior parte delle costanti di informazioni sulle impostazioni locali si escludono a vicenda, è possibile gestire un solo tipo di informazioni alla volta. Le eccezioni a questa regola [usano le impostazioni \_ locali \_ CP \_ ACP](locale-use-cp-acp.md), il [ \_ \_ numero restituito delle impostazioni locali](locale-return-constants.md)e le [impostazioni locali \_ NOUSEROVERRIDE](locale-nouseroverride.md), che possono essere combinate con altre costanti usando un file binario o.

> [!Caution]  
> L'uso delle impostazioni locali \_ NOUSEROVERRIDE è fortemente sconsigliato poiché Disabilita le preferenze dell'utente.

 

Analogamente a una serie di applicazioni, ad esempio Microsoft Active Directory, l'applicazione è in grado di gestire le stringhe in un database ordinabile. Per ulteriori informazioni, vedere [gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Costanti di informazioni sulle impostazioni locali](locale-information-constants.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> <dt>

[Utilizzo di impostazioni locali personalizzate](working-with-custom-locales.md)
</dt> </dl>

 

 



