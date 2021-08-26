---
description: La piattaforma Tablet PC supporta una serie di factoid usati per aumentare l'accuratezza del riconoscimento.
ms.assetid: 9d5fc370-ba58-438b-8850-f31f0f0f6608
title: Factoid supportati dalla versione 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c24c192bcbda04be7ea25deb0c7b1cb7b392de57c43ce7a509e0ceaac31002
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934351"
---
# <a name="supported-factoids-from-version-1"></a>Factoid supportati dalla versione 1

\[Si noti la descrizione seguente dei factoid supportati nella versione 1 di Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK) sono ancora supportati dai riconoscitori, ma è consigliabile che tutti i nuovi sviluppatori (per i riconoscitori di script latini) usino i valori definiti nell'enumerazione [InputScope.](/windows/win32/api/inputscope/ne-inputscope-inputscope)\]

La piattaforma Tablet PC supporta una serie di factoid usati per aumentare l'accuratezza del riconoscimento. Quando si usano factoid, è importante che l'input previsto corrisponda esattamente alla definizione del factoid. Se l'input non corrisponde alla definizione del factoid, l'accuratezza del riconoscimento ne risentirà. Ad esempio, se il factoid **Number** è impostato e l'utente immette lettere, l'accuratezza del riconoscimento per le lettere è scarsa.

Alcuni factoid, ad esempio **Email** e **Digit,** sono quasi identici in tutte le lingue. Altri factoid, ad esempio **Telephone** e **PostalCode,** variano in base alla lingua. Esaminare il formato di ogni factoid per la lingua in uso. Un elenco di formati per ogni factoid in ogni lingua è disponibile nelle tabelle degli argomenti seguenti.

> [!Note]  
> Esiste una sottile ma importante distinzione tra factoid per le lingue occidentali e factoid per le lingue dell'Asia orientale. I factoid per le lingue occidentali vengono implementati usando espressioni che descrivono il risultato desiderato. Il riconoscimento viene quindi distorto per produrre risultati che corrispondono a questa espressione. I factoid per le lingue dell'Asia orientale vengono implementati specificando un intervallo accettabile di caratteri Unicode. Ad esempio, il **factoid Date** per le lingue dell'Asia orientale accetta solo caratteri Unicode all'interno di un determinato intervallo.

 

I factoid per le lingue occidentali includono factoid per inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo. I factoid per le lingue dell'Asia orientale includono factoid per il cinese (semplificato), il cinese (tradizionale), il giapponese e il coreano.

Le sezioni seguenti illustrano i formati supportati per ogni factoid in ogni lingua:

-   [Factoid comuni tra lingue diverse](factoids-common-across-languages.md)
-   [Factoid per le lingue occidentali](factoids-for-western-languages.md)
-   [Factoid per le lingue dell'Asia orientale](factoids-for-east-asian-languages.md)

Se si prevede un input diverso dai formati elencati nelle tabelle di queste sezioni, non usare un factoid. Inoltre, i factoid sono incorporati nel sistema di riconoscimento per ogni lingua. Non è possibile usare factoid di una lingua con un sistema di riconoscimento di un'altra lingua. Ad esempio, non è possibile usare il factoid **Telefono** francese con un riconoscitore giapponese.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Costanti factoid**](factoid-constants.md)
</dt> <dt>

[Classe Microsoft.Ink.Factoid](/previous-versions/ms583657(v=vs.100))
</dt> </dl>

 

 
