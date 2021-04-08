---
description: Accesso alle superfici di DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Accesso alle superfici di DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876973"
---
# <a name="access-to-directdraw-surfaces"></a>Accesso alle superfici di DirectDraw

Gli oggetti multimediali di esempio forniti da VMR ai filtri upstream supportano l'interfaccia [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Per ottenere l'interfaccia, chiamare QueryInterface sull'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) e specificare IID \_ IVMRSurface. I filtri upstream possono quindi usare i metodi IVMRSurface per accedere e modificare la superficie creata da VMR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VMR per gli sviluppatori di filtri DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



