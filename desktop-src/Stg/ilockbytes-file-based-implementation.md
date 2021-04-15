---
title: Implementazione di ILockBytes-File-Based
description: Implementato in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composto COM e progettato per leggere e scrivere direttamente in un file su disco.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implementazioni, basate su file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395478"
---
# <a name="ilockbytes---file-based-implementation"></a>Implementazione di ILockBytes-File-Based

Implementato in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composto COM e progettato per leggere e scrivere direttamente in un file su disco.

## <a name="when-to-use"></a>Utilizzo

I metodi di [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) vengono chiamati dalle implementazioni di file compositi di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) nell'oggetto di archiviazione di file composto creato tramite una chiamata a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), pertanto non è necessario chiamarli direttamente.

## <a name="remarks"></a>Commenti

Di seguito sono riportati i metodi dell'implementazione di File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**
</dt> <dd>

Legge un blocco di byte da un offset specificato all'inizio della matrice di byte.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**
</dt> <dd>

Scrive un blocco di byte da un offset specificato all'inizio della matrice di byte.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**
</dt> <dd>

Garantisce che tutti i buffer interni gestiti dall'implementazione di [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) vengano scritti nell'archiviazione fisica sottostante.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: sesize**
</dt> <dd>

Imposta la dimensione della matrice di byte.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**
</dt> <dd>

Il parametro *dwLockTypes* è impostato su lock \_ ONLYONCE o lock \_ Exclusive, che consente o limita l'accesso alle aree bloccate.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**
</dt> <dd>

Questo metodo sblocca l'area bloccata da [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**
</dt> <dd>

L'implementazione di [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornita da com chiama il metodo [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) per recuperare le informazioni sull'oggetto matrice di byte. Se non esiste un nome ragionevole per la matrice di byte, il metodo **ILockBytes:: stat** fornito da com **restituisce null** nel membro **pwcsName** della struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




