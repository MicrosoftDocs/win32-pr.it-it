---
description: Salvataggio e ripristino di oggetti DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Salvataggio e ripristino di oggetti DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303909"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Salvataggio e ripristino di oggetti DvdState

Gli oggetti [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) consentono alle applicazioni di salvare uno snapshot della sessione utente, incluse informazioni quali il percorso corrente sul disco, il livello padre della persona che sta visualizzando, i flussi audio e di sottoimmagine selezionati e così via. Questo significa che gli utenti possono salvare il proprio posto su un disco DVD-Video e guardarlo in un secondo momento.

Le applicazioni non possono creare oggetti DvdState. Questi oggetti vengono creati internamente dal navigatore DVD quando un'applicazione chiama [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate). Gli oggetti DvdState espongono l'interfaccia [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) per consentire alle applicazioni di eseguire query per determinate informazioni.

Nell'applicazione di esempio DVD le funzioni **CDvdCore:: RestoreBookmark** e **CDvdCore:: SaveBookmark** mostrano come salvare e recuperare gli oggetti DvdState.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



