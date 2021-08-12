---
description: Tipo di posizione di un sommario
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Tipo di posizione di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f94f23e185b46f52123a80a0d27f7fefffcaff7e711a5e9718e07dab7da40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237895"
---
# <a name="the-position-type-of-a-table-of-contents"></a>Tipo di posizione di un sommario

Alcuni metodi [**dell'interfaccia ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) hanno un parametro denominato *enumTocPosType* con un tipo [**di enumerazione TOC \_ POS \_ TYPE**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Questo parametro specifica la posizione in un file multimediale in cui è archiviato un sommario. Lo scopo era che il sommario fosse archiviato nell'intestazione del file o nel corpo del file come oggetto di primo livello. Questa funzionalità non è ancora stata implementata.

Attualmente, i sommari possono essere archiviati solo come oggetti di primo livello, pertanto è sempre necessario impostare il parametro *enumTocPosType* su **TOC \_ POS \_ TOPLEVELOBJECT**. Se si imposta *enumTocPosType* su **TOC \_ POS \_ INHEADER,** il metodo restituirà **E \_ NOTIMPL.**

I metodi seguenti hanno un *parametro enumTocPosType.*

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori del parser sommario](toc-parser-programming-guide.md)
</dt> </dl>

 

 



