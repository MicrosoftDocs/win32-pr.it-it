---
title: IFillLockBytes - Implementazione
description: Il sistema fornisce un'implementazione di IFillLockBytes come parte dell'implementazione di file composti.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- Implementazione di IFillLockBytes Strctd Stg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c095d32bf9a932062b527cd486ee518e099d8de0f0d859caf2f1143e68237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663021"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes - Implementazione

Il sistema fornisce [**un'implementazione di IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) come parte dell'implementazione di file composti.

Il download del codice può creare un'istanza di un oggetto File composto asincrono chiamando [**StgOpenAsyncDocFileOnIFillLockBytes.**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes) Il download del codice può anche creare un'istanza di un oggetto wrapper di matrice di byte asincrono in un file o una matrice di byte esistente chiamando la funzione [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) o la funzione [**StgGetIFillLockBytesOnILockBytes.**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes)

## <a name="when-to-use"></a>Utilizzo

Attualmente, i moniker URL sono gli unici utenti dell'implementazione dell'archiviazione asincrona COM.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i quattro metodi [**dell'implementazione di IFillLockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

Scrive un nuovo blocco di byte alla fine di una matrice di byte. Le dimensioni del blocco vengono specificate come parametro per [**FillAppend.**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

Scrive un nuovo blocco di dati in una posizione specificata nella matrice di byte.

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**
</dt> <dd>

Imposta le dimensioni della matrice di byte. Restituisce E \_ FAIL dalle chiamate a [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) che tentano di accedere ai dati oltre il limite superiore specificato dal metodo .

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**
</dt> <dd>

Informa la matrice di byte che un download è stato terminato, con esito positivo o negativo.

</dd> </dl>

 

 




