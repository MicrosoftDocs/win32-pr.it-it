---
description: Definisce un metodo che determina se la shell sarà consentita per lo spostamento, la copia, l'eliminazione o la ridenominazione di una cartella nella radice di sincronizzazione di un provider di cloud.
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
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400496"
---
# <a name="istorageprovidercopyhook-interface"></a>Interfaccia IStorageProviderCopyHook

Espone un metodo che determina se la shell sarà consentita per lo spostamento, la copia, l'eliminazione o la ridenominazione di una cartella nella radice di sincronizzazione di un provider di cloud.

## <a name="members"></a>Membri

L'interfaccia **IStorageProviderCopyHook** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IStorageProviderCopyHook** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IStorageProviderCopyHook** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Determina se la shell sarà autorizzata a spostare, copiare, eliminare o rinominare una cartella nella radice di sincronizzazione di un provider cloud.                                                           |


## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 10 Insider Preview Build 19624                                                |
| Intestazione<br/>                   | ShObjIdl. h   |
