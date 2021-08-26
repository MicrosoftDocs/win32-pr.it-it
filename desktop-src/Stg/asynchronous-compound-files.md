---
title: File compositi asincroni
description: File compositi asincroni, l'implementazione fornita dal sistema di archiviazione asincrona, consente il download efficiente di file composti da Internet in generale e dal Web in particolare.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15404f33041fb52f5baa5230f69434ce390b985c41374235c1f3979ef6c2f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034987"
---
# <a name="asynchronous-compound-files"></a>File compositi asincroni

File compositi asincroni, l'implementazione fornita dal sistema di archiviazione asincrona, consente il download efficiente di file composti da Internet in generale e dal Web in particolare. L'architettura di base dei file compositi asincroni è illustrata nel diagramma seguente.

![Architettura di base dei file compositi asincroni](images/asy-stor.png)

L'implementazione di file compositi asincroni può funzionare con nuovi tipi di moniker asincroni che comprendono i protocolli Internet e possono essere associati a un oggetto identificato da un URL. Tale moniker restituirebbe un puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) asincrono dalla chiamata del client a [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).

I file compositi in generale vengono implementati su un oggetto matrice di byte, un'astrazione di un file che rappresenta i dati di un oggetto come matrice di byte flat. L'oggetto matrice di byte espone le funzionalità tramite [**l'interfaccia ILockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Se una matrice di byte supporta l'archiviazione asincrona non bloccante, restituisce E PENDING all'implementazione del file composto, che a sua volta propaga l'errore \_ al chiamante.

Per tenere traccia dei dati disponibili durante un download, una matrice di byte che supporta l'archiviazione asincrona espone [**l'interfaccia IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) su un oggetto wrapper fornito dal sistema specificamente a questo scopo. Il codice di download fornito da un moniker asincrono chiama questa interfaccia per riempire la matrice di byte in modo asincrono, in quanto i dati sono disponibili. L'oggetto wrapper espone anche **un'interfaccia ILockBytes,** utilizzata dall'implementazione asynchronous compound files per leggere e scrivere dati da e nella matrice.

Gli oggetti di flusso e di archiviazione asincroni forniscono un punto di connessione per [**l'interfaccia IProgressNotify,**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) implementata dal codice di download del moniker asincrono. L'implementazione asynchronous compound files chiama **IProgressNotify** per fornire al downloader informazioni sullo stato dell'operazione di download.

 

 