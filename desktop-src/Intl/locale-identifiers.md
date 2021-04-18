---
description: Ogni impostazioni locali dispone di un identificatore univoco, un valore a 32 bit costituito da un identificatore di lingua e un identificatore di ordinamento.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificatori delle impostazioni locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305638"
---
# <a name="locale-identifiers"></a>Identificatori delle impostazioni locali

Ogni [impostazioni locali](locales-and-languages.md) dispone di un identificatore univoco, un valore a 32 bit costituito da un identificatore di [lingua](language-identifiers.md) e un [identificatore di ordinamento](sort-order-identifiers.md). L'identificatore delle impostazioni locali è un'abbreviazione numerica internazionale standard e include i componenti necessari per identificare in modo univoco una delle impostazioni locali definite dal sistema operativo installate. NLS supporta sia gli identificatori delle impostazioni locali predefiniti sia gli identificatori personalizzati.

> [!Note]  
> I nomi delle impostazioni locali possono essere utilizzati con le funzioni introdotte in Windows Vista che accettano un [nome delle impostazioni locali](locale-names.md) come parametro, anziché un identificatore delle impostazioni locali. Per ulteriori informazioni, vedere [chiamata delle funzioni "nome delle impostazioni locali"](calling-the--locale-name--functions.md). L'uso di nomi delle impostazioni locali invece degli identificatori delle impostazioni locali è sempre preferibile.

 

Nella figura seguente viene illustrato il formato dei bit in un identificatore delle impostazioni locali.

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a>Identificatori delle impostazioni locali predefiniti

Gli identificatori delle impostazioni locali predefiniti supportati da NLS sono definiti nelle informazioni di [riferimento sulle API NLS (National Language Support)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

NLS Usa le seguenti costanti di informazioni sulle impostazioni locali per rappresentare gli identificatori delle impostazioni locali.

-   [Impostazioni \_ locali SLANGUAGE](locale-slanguage.md) o [impostazioni locali \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)
-   [impostazioni locali \_ sname](locale-sname.md)
-   [impostazioni locali \_ SSCRIPTS](locale-sscripts.md)
-   [impostazioni locali \_ IDEFAULTANSICODEPAGE](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a>Identificatori delle impostazioni locali personalizzati

**Windows Vista:** NLS supporta gli identificatori delle impostazioni locali personalizzati rappresentati dalle seguenti costanti di informazioni sulle impostazioni locali.

-   [impostazioni locali \_ personalizzate \_ predefinite](locale-custom-constants.md)
-   [\_ \_ impostazione predefinita interfaccia utente personalizzata impostazioni locali \_](locale-custom-constants.md)
-   [impostazioni locali \_ personalizzate non \_ specificate](locale-custom-constants.md)

## <a name="building-a-locale"></a>Creazione di impostazioni locali

È possibile usare l'utilità del compilatore delle impostazioni locali fornita da NLS per compilare le impostazioni locali. Per altre informazioni, vedere [Generatore di impostazioni locali Microsoft](https://www.microsoft.com/download/details.aspx?id=41158).

L'applicazione può costruire un identificatore delle impostazioni locali usando la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) . In alternativa, è possibile usare uno degli identificatori predefiniti corrispondenti alle costanti elencate di seguito.

-   [impostazioni locali \_ INvariabili](locale-invariant.md)
-   [impostazioni locali del \_ sistema \_](locale-system-default.md)
-   [\_impostazione predefinita utente impostazioni locali \_](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a>Recupero degli identificatori delle impostazioni locali

Un'applicazione può recuperare gli identificatori delle impostazioni locali correnti usando le funzioni [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) e [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) . Ogni thread può impostare e recuperare le proprie impostazioni locali con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) e [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Identificatori di lingua](language-identifiers.md)
</dt> <dt>

[Nomi delle impostazioni locali](locale-names.md)
</dt> <dt>

[Identificatori di ordinamento](sort-order-identifiers.md)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
