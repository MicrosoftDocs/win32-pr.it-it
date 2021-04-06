---
title: Per arrestare l'indicizzazione in corso
description: Per arrestare l'indicizzazione in corso
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media Format SDK, arresto dell'indicizzazione in corso
- ASF (Advanced Systems Format), arresto dell'indicizzazione in corso
- ASF (formato avanzato dei sistemi), arresto dell'indicizzazione in corso
- indici, arresto dell'indicizzazione in corso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea40cbf020182250e0fb982af5b5f84327d5d9a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046330"
---
# <a name="to-stop-indexing-in-progress"></a>Per arrestare l'indicizzazione in corso

Dopo l'avvio dell'indicizzazione con una chiamata a [**IWMIndexer:: startindexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), l'indicizzatore continuerà a continuare fino a quando il file non sarà indicizzato. È possibile arrestare le operazioni di indicizzazione chiamando il metodo [**IWMIndexer:: Cancel**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) . Dopo aver annullato l'indicizzazione, è possibile chiamare di nuovo la funzione **startIndex** , ma l'indicizzatore inizierà dall'inizio del file anziché riprendere dal punto di annullamento.

Poiché la funzione **startIndex** è una chiamata asincrona, in genere è necessario chiamare **Cancel** da un altro thread o gestore eventi nell'applicazione. In genere l' **annullamento** verrà chiamato da una routine di evento associata a un controllo Button di un'applicazione Windows.

Quando l'indicizzazione viene annullata, l'indicizzatore passa un messaggio di stato WMT \_ chiuso, come se il file fosse stato indicizzato correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




