---
description: Recupero e impostazione delle informazioni sulle impostazioni locali
ms.assetid: 7675f826-76be-4361-a82c-9573040a7e72
title: Recupero e impostazione delle informazioni sulle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d02c2bb58328529781309ce8284310acbcb6fb545ecdc076df295cd020344a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130311"
---
# <a name="retrieving-and-setting-locale-information"></a>Recupero e impostazione delle informazioni sulle impostazioni locali

L'applicazione deve essere in grado di recuperare e impostare informazioni specifiche sulle impostazioni [locali e sulle lingue disponibili.](locales-and-languages.md) Ogni elemento delle informazioni sulle impostazioni locali, ad esempio il nome di un determinato giorno della settimana o il carattere usato come separatore decimale, ha una costante corrispondente. Le costanti disponibili sono definite in [Costanti di informazioni sulle impostazioni locali](locale-information-constants.md).

L'applicazione archivia e modifica sempre le informazioni sulle impostazioni locali come stringa con terminazione Null. Non sono consentiti dati binari e i valori numerici devono essere specificati come testo. Ogni tipo di informazioni ha un formato specifico. Inoltre, diversi tipi sono collegati tra loro in modo che la modifica di un tipo cambi anche il valore dell'altro tipo.

Per recuperare informazioni sulle impostazioni locali, l'applicazione chiama [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la costante che corrisponde alle informazioni necessarie. L'applicazione può chiamare [**SetLocaleInfo per**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) impostare un elemento di informazioni sulle impostazioni locali.

> [!Note]  
> Anche se [un identificatore delle impostazioni](locale-identifiers.md) locali potrebbe essere supportato, non è disponibile per l'uso da parte di un'applicazione, a meno che non siano installate anche le impostazioni locali corrispondenti.

 

Poiché la maggior parte delle costanti di informazioni sulle impostazioni locali si escludono a vicenda, è possibile gestire un solo tipo di informazioni alla volta. Le eccezioni a questa regola sono [LOCALE \_ USE CP \_ \_ ACP,](locale-use-cp-acp.md) [LOCALE RETURN \_ \_ NUMBER](locale-return-constants.md)e [LOCALE \_ NOUSEROVERRIDE,](locale-nouseroverride.md)che possono essere combinate con altre costanti usando un or binario.

> [!Caution]  
> L'uso \_ di LOCALE NOUSEROVERRIDE è fortemente sconsigliato perché disabilita le preferenze utente.

 

Analogamente a un certo numero di applicazioni, ad esempio Microsoft Active Directory, l'applicazione può mantenere le stringhe in un database ordinabile. Per altre informazioni, vedere [Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> <dt>

[Costanti di informazioni sulle impostazioni locali](locale-information-constants.md)
</dt> <dt>

[Gestione dell'ordinamento nelle applicazioni](handling-sorting-in-your-applications.md)
</dt> <dt>

[Uso delle impostazioni locali personalizzate](working-with-custom-locales.md)
</dt> </dl>

 

 



