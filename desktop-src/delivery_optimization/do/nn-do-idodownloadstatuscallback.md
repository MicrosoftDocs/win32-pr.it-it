---
title: Interfaccia IDODownloadStatusCallback
description: Usato per ricevere notifiche su un download.
keywords:
- Interfaccia IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: d91ff44e3b4f4247983ec81d53257347c8bcfa523f85855dcd0d37074f4b38fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498951"
---
# <a name="idodownloadstatuscallback-interface"></a>Interfaccia IDODownloadStatusCallback

**L'interfaccia IDODownloadStatusCallback** viene usata per ricevere notifiche su un download.

## <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IDODownloadStatusCallback.**

| Metodo | Descrizione |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | DO chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato di download. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | Do.h |