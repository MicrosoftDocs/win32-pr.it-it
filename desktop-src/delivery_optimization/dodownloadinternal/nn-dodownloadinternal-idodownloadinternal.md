---
title: Interfaccia IDODownloadInternal
description: Usato per ottenere o impostare le proprietà di download estese.
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
ms.openlocfilehash: de9079f7b87822ce950bc4e6c3ece6457e62775c32f7c0d51e76959332298bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755781"
---
# <a name="idodownloadinternal-interface"></a>Interfaccia IDODownloadInternal

> [!IMPORTANT]
> **L'interfaccia IDODownloadInternal** è deprecata. Usare invece [l'interfaccia IDODownload.](../do/nn-do-idodownload.md)

**L'interfaccia IDODownloadInternal** viene usata per ottenere o impostare le proprietà di download estese.

## <a name="methods"></a>Metodi

**L'interfaccia IDODownloadInternal** include questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDODownloadInternal::GetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | Recupera un puntatore a un **variant che** contiene un valore della proprietà di download esteso specifico. |
| [IDODownloadInternal::SetPropertyEx](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | Imposta una proprietà di download estesa. Il metodo accetta un puntatore a **un variant** che contiene un valore di proprietà specifico da applicare al download. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, versione 1809 \[ Solo applicazioni Win32\] |
| **Intestazione** | DODownloadInternal.h |