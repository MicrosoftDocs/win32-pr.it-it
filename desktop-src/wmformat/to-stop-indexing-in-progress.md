---
title: Per arrestare l'indicizzazione in corso
description: Per arrestare l'indicizzazione in corso
ms.assetid: 76c641fa-ea00-4035-bc30-a92059da584a
keywords:
- Windows Media Format SDK, arresto dell'indicizzazione in corso
- Advanced Systems Format (ASF), arresto dell'indicizzazione in corso
- ASF (Advanced Systems Format), arresto dell'indicizzazione in corso
- indici, arresto dell'indicizzazione in corso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d441e42bc3c7033e776d353cf64fc5938183a4f8d720f086b4fb5fd9828be02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432624"
---
# <a name="to-stop-indexing-in-progress"></a>Per arrestare l'indicizzazione in corso

Dopo aver avviato l'indicizzazione con una chiamata a [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing), l'indicizzatore continuerà normalmente fino a quando il file non viene indicizzato. È possibile arrestare le operazioni di indicizzazione chiamando il [**metodo IWMIndexer::Cancel.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-cancel) Dopo aver annullato l'indicizzazione, è possibile chiamare di nuovo **StartIndexing,** ma l'indicizzatore inizierà dall'inizio del file anziché riprendere dal punto di annullamento.

Poiché **StartIndexing** è una chiamata asincrona, in genere è necessario chiamare **Cancel** da un altro thread o gestore eventi nell'applicazione. In **genere Cancel** viene chiamato da una routine evento associata a un controllo pulsante di un'Windows app.

Quando l'indicizzazione viene annullata, l'indicizzatore passerà un messaggio di stato WMT CLOSED, proprio come se il \_ file fosse stato indicizzato correttamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




