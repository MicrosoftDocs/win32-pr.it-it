---
title: Interfaccia IDODownloadStatusCallback
description: Utilizzato per ricevere notifiche relative a un download.
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
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399078"
---
# <a name="idodownloadstatuscallback-interface"></a>Interfaccia IDODownloadStatusCallback

L'interfaccia **IDODownloadStatusCallback** viene utilizzata per ricevere notifiche relative a un download.

## <a name="methods"></a>Metodi

L'interfaccia **IDODownloadStatusCallback** dispone di questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDODownloadStatusCallback::OnStatusChanged](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | Chiama l'implementazione di questo metodo ogni volta che viene modificato lo stato del download. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |