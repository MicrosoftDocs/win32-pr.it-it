---
description: Identificazione di operazioni DVD valide
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificazione di operazioni DVD valide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401283"
---
# <a name="identifying-valid-dvd-operations"></a>Identificazione di operazioni DVD valide

Diversi fattori determinano se è possibile eseguire un'operazione DVD specifica:

-   Dominio corrente. Alcuni comandi sono validi solo in alcuni domini. Quando il dominio viene modificato, lo strumento di spostamento Invia un \_ evento di modifica del dominio DVD EC \_ \_ . È anche possibile chiamare [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) per ottenere il dominio corrente.
-   Flag UOPS. Si tratta di flag scritti sul disco che indicano quali operazioni sono consentite. Ogni volta che i flag cambiano, lo strumento di spostamento Invia un \_ \_ \_ evento di modifica UOPs valido del DVD EC \_ con i nuovi flag. È anche possibile chiamare [**IDvdInfo2:: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) per ottenere i flag UOPs correnti.
-   Contenuto DVD. Alcuni comandi potrebbero non essere rilevanti in base al contenuto del DVD. Ad esempio, il metodo [**IDVDControl2:: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) può essere consentito in base ai flag Domain e UOPs correnti, ma il video potrebbe avere solo un angolo. In tal caso, la chiamata **SelectAngle** è consentita ma non è un'opzione significativa.

In caso di dubbio, consentire un'azione. Nel peggiore dei casi, il metodo [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) avrà esito negativo ed è possibile inviare commenti e suggerimenti all'utente. Il feedback dovrebbe essere relativamente discreto. Ad esempio, è possibile che si lampeggi una piccola X rossa per avvisare l'utente. Il navigatore DVD restituisce VFW \_ e \_ DVD \_ INVALIDDOMAIN quando il dominio vieta un'operazione e l' \_ operazione VFW e DVD viene \_ \_ \_ inibita quando i flag UOPs proibiscono un'operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



