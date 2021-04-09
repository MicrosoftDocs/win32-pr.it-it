---
title: Interfaccia IDODownloadInternal
description: Utilizzato per ottenere o impostare le proprietà di download estese.
keywords:
- Interfaccia IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118126"
---
# <a name="idodownloadinternal-interface"></a>Interfaccia IDODownloadInternal

> [!IMPORTANT]
> L'interfaccia **IDODownloadInternal** è deprecata. Usare invece l'interfaccia [IDODownload](../do/nn-do-idodownload.md) .

L'interfaccia **IDODownloadInternal** viene utilizzata per ottenere o impostare le proprietà di download estese.

## <a name="methods"></a>Metodi

L'interfaccia **IDODownloadInternal** dispone di questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Recupera un puntatore a un **Variant** che contiene un valore di proprietà di download esteso specifico. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Imposta una proprietà di download estesa. Il metodo accetta un puntatore a una **variante** che contiene un valore della proprietà specifico da applicare al download. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | DODownloadInternal. h |