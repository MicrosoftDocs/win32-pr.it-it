---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221504"
---
# <a name="toomanychildren"></a>TooManyChildren

## <a name="text"></a>Testo

Arrestato ricerca di elementi di pari livello aggiuntivi dopo la ricerca di elementi di {0} pari livello. Possibile albero errato

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

L'albero degli elementi potrebbe essere ciclico e il livello di profondità dell'albero è infinito.

Questo problema può causare problemi di navigazione per gli strumenti automatizzati, in quanto verranno immessi elementi che sembrano essere un riferimento circolare o un ciclo infinito.

## <a name="possible-causes"></a>Possibili cause

-   La progettazione dell'applicazione o del controllo potrebbe essere troppo complessa. Questo avviso può essere segnalato per i controlli di visualizzazione elenco con un numero elevato di elementi. In questi casi, in genere è possibile ignorare questo avviso.
-   Implementazione MSAA non corretta o non valida.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




