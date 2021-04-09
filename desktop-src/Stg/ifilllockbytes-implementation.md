---
title: IFillLockBytes-implementazione
description: Il sistema fornisce un'implementazione di IFillLockBytes come parte dell'implementazione dei file composti.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd STG, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955439"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes-implementazione

Il sistema fornisce un'implementazione di [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) come parte dell'implementazione dei file composti.

Il download del codice può creare un'istanza di un oggetto file composto asincrono chiamando [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes). Il download del codice può anche creare un'istanza di un oggetto wrapper della matrice di byte asincrona su un file o una matrice di byte esistente chiamando la funzione [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) o [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) .

## <a name="when-to-use"></a>Utilizzo

Attualmente, i moniker URL sono gli unici utenti dell'implementazione di archiviazione asincrona COM.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i quattro metodi dell'implementazione di [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) .

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes:: FillAppend**
</dt> <dd>

Scrive un nuovo blocco di byte alla fine di una matrice di byte. La dimensione del blocco viene specificata come parametro per [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes:: FillAt**
</dt> <dd>

Scrive un nuovo blocco di dati in una posizione specificata nella matrice di byte.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes:: SetFillSize**
</dt> <dd>

Imposta la dimensione della matrice di byte. Restituisce E \_ non vengono eseguite chiamate a [**ILockBytes:: ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) che tentano di accedere ai dati oltre il limite massimo specificato dal metodo.

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes:: terminate**
</dt> <dd>

Informa la matrice di byte che un download è stato terminato, con esito positivo o negativo.

</dd> </dl>

 

 




