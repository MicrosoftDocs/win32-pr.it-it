---
description: La piattaforma Tablet PC supporta un numero di factoids che vengono utilizzati per aumentare l'accuratezza del riconoscimento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoids supportati dalla versione 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad6d08b91a457d38a3eb8543200eb1919eb2bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319140"
---
# <a name="supported-factoids-from-version-1"></a>Factoids supportati dalla versione 1

\[Tenere presente che la descrizione di factoids supportata nella versione 1 del Software Development Kit (SDK) di Microsoft Windows XP Tablet PC Edition è ancora supportata dai sistemi di riconoscimento, ma è consigliabile che tutti i nuovi sviluppatori (per i riconoscitori dello script latino) usino i valori definiti nell'enumerazione [InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope) .\]

La piattaforma Tablet PC supporta un numero di factoids che vengono utilizzati per aumentare l'accuratezza del riconoscimento. Quando si usa factoids, è importante che l'input previsto corrisponda esattamente alla definizione del controllo del controllo. Se l'input non corrisponde alla definizione del controllo del controllo, l'accuratezza del riconoscimento soffre. Se, ad esempio, il controllo di controllo **numerico** è impostato e l'utente immette lettere, l'accuratezza del riconoscimento per le lettere è insufficiente.

Alcuni factoids, ad esempio la **posta elettronica** e la **cifra**, sono quasi identici in tutte le lingue. Altri factoids, ad esempio **telefono** e **Cap**, variano in base alla lingua. Esaminare il formato di ogni controllo oggetto per la lingua in uso. Un elenco di formati per ogni controllo oggetto in ogni lingua è disponibile nelle tabelle degli argomenti che seguono questo argomento.

> [!Note]  
> Esiste una differenza sottile ma importante tra factoids per le lingue occidentali e factoids per le lingue asiatiche orientali. Factoids per le lingue occidentali vengono implementate usando espressioni che descrivono il risultato desiderato. Il riconoscimento viene quindi distorto per produrre risultati corrispondenti a questa espressione. Factoids per le lingue asiatiche orientali vengono implementate specificando un intervallo di caratteri Unicode accettabile. Ad esempio, il controllo della **Data** per le lingue asiatiche orientali accetta solo caratteri Unicode in un determinato intervallo.

 

Factoids per le lingue occidentali includono factoids per la lingua inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo. Factoids per le lingue asiatiche orientali includono factoids per il cinese (semplificato), cinese (tradizionale), giapponese e coreano.

Nelle sezioni seguenti vengono illustrati i formati supportati per ogni controllo oggetto in ogni lingua:

-   [Factoids comuni tra lingue diverse](factoids-common-across-languages.md)
-   [Factoids per le lingue occidentali](factoids-for-western-languages.md)
-   [Factoids per le lingue asiatiche orientali](factoids-for-east-asian-languages.md)

Se si prevede un input diverso dai formati elencati nelle tabelle di queste sezioni, non usare un controllo del controllo. Inoltre, factoids sono incorporati nel riconoscimento per ogni lingua. Non è possibile usare factoids da un linguaggio con un riconoscimento da un altro linguaggio. Non è ad esempio possibile utilizzare il controllo del **telefono** francese con un riconoscimento giapponese.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti controllo oggetto**](factoid-constants.md)
</dt> <dt>

[Classe Microsoft. Ink. controllore](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
