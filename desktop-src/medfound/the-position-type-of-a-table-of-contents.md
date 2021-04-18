---
description: Tipo di posizione di un sommario
ms.assetid: cc2fbadc-43f7-470c-873b-de2dc9d84e5d
title: Tipo di posizione di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1b6782a3722a6ce5a36117694f35442f8e4d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310204"
---
# <a name="the-position-type-of-a-table-of-contents"></a>Tipo di posizione di un sommario

Alcuni metodi dell'interfaccia [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) hanno un parametro denominato *enumTocPosType* che dispone di un tipo di [**\_ \_ tipo POS del sommario enum**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-toc_pos_type). Questo parametro specifica la posizione in un file multimediale in cui è archiviato un sommario. Lo scopo è che il sommario possa essere archiviato nell'intestazione del file o nel corpo del file come oggetto di primo livello. Questa funzionalità non è stata ancora implementata.

Attualmente, le tabelle di contenuto possono essere archiviate solo come oggetti di primo livello, quindi è sempre necessario impostare il parametro *enumTocPosType* su **TOC \_ POS \_ TOPLEVELOBJECT**. Se si imposta *enumTocPosType* su **TOC \_ POS \_ inheader**, il metodo restituirà **E \_ NOTIMPL**.

I metodi seguenti hanno un parametro *enumTocPosType* .

-   [**GetTocCount**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettoccount)
-   [**GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
-   [**GetTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbytype)
-   [**AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc)
-   [**RemoveTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbyindex)
-   [**RemoveTocByType**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-removetocbytype)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori del parser Sommario](toc-parser-programming-guide.md)
</dt> </dl>

 

 



