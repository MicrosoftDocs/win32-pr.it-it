---
description: Definisce un metodo che determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider di servizi cloud.
title: Interfaccia IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: aa26a329bd80295a6a46a1bb11d1dc651baf1ea71975576ed704b29a7fee8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968870"
---
# <a name="istorageprovidercopyhook-interface"></a>Interfaccia IStorageProviderCopyHook

Espone un metodo che determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider di servizi cloud.

## <a name="members"></a>Membri

**L'interfaccia IStorageProviderCopyHook** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IStorageProviderCopyHook** include anche questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IStorageProviderCopyHook** include questi metodi.



| Metodo                                           | Descrizione                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider di servizi cloud.                                                           |


## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 10 Insider Preview Build 19624                                                |
| Intestazione<br/>                   | shobjidl.h   |
