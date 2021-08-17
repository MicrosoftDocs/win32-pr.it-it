---
description: Salvataggio e ripristino di oggetti DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Salvataggio e ripristino di oggetti DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 922851cce72f736364c1f1e66b24032586221ad9cb75494c7286fe962eb34403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982571"
---
# <a name="saving-and-restoring-dvdstate-objects"></a>Salvataggio e ripristino di oggetti DvdState

Gli [**oggetti IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) consentono alle applicazioni di salvare uno snapshot della sessione utente, incluse informazioni quali la posizione corrente sul disco, il livello di genitoria della persona che visualizza, i flussi audio e secondari selezionati e così via. Ciò significa che gli utenti possono salvare il proprio posto in un disco DVD-Video e guardarlo in un secondo momento.

Le applicazioni non possono creare oggetti DvdState. Questi oggetti vengono creati internamente dallo strumento di spostamento DVD quando un'applicazione chiama [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate). Gli oggetti DvdState espongono [**l'interfaccia IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) per consentire alle applicazioni di eseguire query per determinate informazioni.

Nell'applicazione di esempio DVD le funzioni **CDvdCore::RestoreBookmark** e **CDvdCore::SaveBookmark** mostrano come salvare e recuperare oggetti DvdState.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



