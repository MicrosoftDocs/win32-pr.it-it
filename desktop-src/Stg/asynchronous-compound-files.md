---
title: File composti asincroni
description: I file composti asincroni, l'implementazione fornita dal sistema di archiviazione asincrona, consentono il download efficiente di file composti da Internet in generale e il Web in particolare.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04de2162b50283b12bc8deed6ec908d92e7584d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399502"
---
# <a name="asynchronous-compound-files"></a>File composti asincroni

I file composti asincroni, l'implementazione fornita dal sistema di archiviazione asincrona, consentono il download efficiente di file composti da Internet in generale e il Web in particolare. Il diagramma seguente illustra l'architettura di base dei file composti asincroni.

![architettura di base dei file composti asincroni](images/asy-stor.png)

L'implementazione asincrona dei file composti può funzionare con nuovi tipi di moniker asincroni che conoscono i protocolli Internet e possono essere associati a un oggetto identificato da un URL. Tale moniker restituisce un puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) asincrono dalla chiamata del client a [**IMoniker:: BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).

I file composti in generale vengono implementati sopra un oggetto matrice di byte, un'astrazione di un file che rappresenta i dati di un oggetto come matrice di byte flat. L'oggetto matrice di byte ne espone la funzionalità tramite l'interfaccia [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) . Se una matrice di byte supporta l'archiviazione asincrona non bloccata, restituisce E in \_ sospeso all'implementazione del file composto, che a sua volta propaga di nuovo l'errore al chiamante.

Per tenere traccia dei dati disponibili durante il download, una matrice di byte che supporta l'archiviazione asincrona espone l'interfaccia [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) su un oggetto wrapper fornito dal sistema in modo specifico per questo scopo. Il codice di download fornito da un moniker asincrono chiama questa interfaccia per riempire la matrice di byte in modo asincrono, perché i dati sono disponibili. L'oggetto wrapper espone anche un'interfaccia **ILockBytes** , che viene usata dall'implementazione asincrona dei file composti per leggere e scrivere dati da e verso la matrice.

Gli oggetti di archiviazione e di flusso asincroni forniscono un punto di connessione per l'interfaccia [**IProgressNotify**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) , implementata dal codice di download del moniker asincrono. L'implementazione asincrona dei file composti chiama **IProgressNotify** per fornire al Downloader informazioni sullo stato dell'operazione di download.

 

 