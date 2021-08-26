---
description: Identificazione di operazioni DVD valide
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificazione di operazioni DVD valide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd1b99a38949ca0ff54d391e9ad5458bbe854a5c4af4140b15deaf4177147aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051981"
---
# <a name="identifying-valid-dvd-operations"></a>Identificazione di operazioni DVD valide

Diversi fattori determinano se è possibile eseguire un'operazione DVD specifica:

-   Dominio corrente. Alcuni comandi sono validi solo in determinati domini. Quando il dominio viene modificato, lo strumento di navigazione invia un evento EC \_ DVD \_ DOMAIN \_ CHANGE. È anche possibile chiamare [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) per ottenere il dominio corrente.
-   Flag UOPS. Si tratta di flag scritti sul disco che indicano quali operazioni sono consentite. Ogni volta che i flag cambiano, lo strumento di navigazione invia un evento EC \_ DVD \_ VALID \_ UOPS \_ CHANGE con i nuovi flag. È anche possibile chiamare [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) per ottenere i flag UOPS correnti.
-   Contenuto DVD. Alcuni comandi potrebbero non essere pertinenti in base al contenuto del DVD. Ad esempio, il [**metodo IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) potrebbe essere consentito in base al dominio corrente e ai flag UOPS, ma il video potrebbe avere un solo angolo. In tal caso, la **chiamata SelectAngle** è consentita, ma non è un'opzione significativa.

In caso di dubbi, consentire un'azione. Nel peggiore dei casi, [**il metodo IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) avrà esito negativo ed è possibile inviare commenti e suggerimenti all'utente. Il feedback dovrebbe essere relativamente discreto. Ad esempio, è possibile eseguire il flash di una piccola X rossa per avvisare l'utente. Lo strumento di navigazione DVD restituisce VFW E DVD INVALIDDOMAIN quando il dominio impedisce un'operazione e \_ \_ \_ VFW E DVD OPERATION INIBITO quando i flag UOPS impediscono \_ \_ \_ \_ un'operazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



