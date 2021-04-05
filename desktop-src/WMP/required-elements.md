---
title: Elementi obbligatori
description: Elementi obbligatori
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Interfacce di Windows Media Player Mobile, elementi
- interfacce, elementi
- file di definizione dell'interfaccia, elementi
- elementi, file di definizione dell'interfaccia
- elementi, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710876"
---
# <a name="required-elements"></a>Elementi obbligatori

È necessario specificare gli elementi seguenti nel file di definizione dell'interfaccia utente:

-   **Intestazione.** L'intestazione del file di definizione dell'interfaccia principale è obbligatoria. Per informazioni sulla versione dell'intestazione, vedere la tabella nella sezione [creazione di un file di definizione dell'interfaccia](creating-a-skin-definition-file.md) .
-   **Sezione Descrizione.** La sezione Descrizione è obbligatoria per la creazione di interfacce per Windows Media Player 9 serie per Windows Mobile. Deve essere la prima sezione del file di definizione dell'interfaccia e deve specificare valori validi per le dimensioni. La specifica di un valore per l'orientamento è facoltativa.
-   **Sezione bitmap.** La sezione bitmap è obbligatoria. Inoltre, la sezione bitmap deve specificare nomi validi per i file di sfondo, disabilitato, push, area e immagine superata.
-   **file di immagine.** Come parte dell'interfaccia, è necessario fornire i file di sfondo, disabilitato, di push, di area e di immagine con privilegi avanzati. Se si creano interfacce per Windows Media Player 10 mobile o versioni successive, non è necessario includere i file di area o di immagine super.

Se si crea un'interfaccia con solo immagini definite, l'interfaccia sarà visibile, ma non offrirà alcuna funzionalità significativa all'utente. Se si decide di creare un'interfaccia senza pulsanti, ad esempio per impedire all'utente di ignorare un determinato contenuto, tenere presente che potrebbe essere ancora possibile eseguire il mapping delle funzionalità ai pulsanti hardware del dispositivo.

I file Thumb sono obbligatori e i TrackBar non possono essere usati senza Thumb.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di definizione dell'interfaccia**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




