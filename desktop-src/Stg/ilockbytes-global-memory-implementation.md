---
title: ILockBytes - Implementazione della memoria globale
description: L'implementazione della memoria globale ILockBytes viene implementata in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composti COM e progettata per leggere e scrivere direttamente nella memoria globale.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd Stg , implementazioni, memoria globale
- ILockBytes Strctd Stg , implementazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f9786f29433bcc02e0b56f3ea9d45c949593f60962e80a650d80ed625da41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867450"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes - Implementazione della memoria globale

L'implementazione della memoria globale ILockBytes viene implementata in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composti COM e progettata per leggere e scrivere direttamente nella memoria globale.

## <a name="when-to-use"></a>Utilizzo

I metodi [**di ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) vengono chiamati dalle implementazioni di file composti [**di IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) sull'oggetto di archiviazione file composto creato tramite una chiamata a [**StgCreateDocfile.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)

## <a name="remarks"></a>Commenti

Di seguito sono riportati i metodi dell'implementazione della memoria [**globale ILockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**
</dt> <dd>

Legge un blocco di byte da un offset specificato all'inizio della matrice di byte.

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**
</dt> <dd>

Scrive il blocco di byte da un offset specificato all'inizio della matrice di byte.

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**
</dt> <dd>

A differenza dell'implementazione basata su file, la chiamata di questo metodo nell'implementazione della memoria globale non ha alcun effetto.

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**
</dt> <dd>

Imposta le dimensioni della matrice di byte.

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**
</dt> <dd>

Questa implementazione non supporta il blocco, quindi *dwLocksType* è impostato su zero. Il chiamante deve assicurarsi che gli accessi siano validi e si escludono a vicenda.

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**
</dt> <dd>

Questa implementazione non supporta il blocco.

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**
</dt> <dd>

L'implementazione [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornita da COM chiama il metodo [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) per recuperare i dati sull'oggetto matrice di byte. Se non esiste un nome ragionevole per la matrice di byte, il metodo **ILockBytes::Stat** fornito da COM restituisce **NULL** nel membro **pwcsName** della [**struttura STATSTG.**](/windows/win32/api/objidl/ns-objidl-statstg)

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




