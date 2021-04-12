---
title: Interfaccia IDODownload
description: Utilizzato per avviare e gestire un download.
keywords:
- Interfaccia IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337646"
---
# <a name="idodownload-interface"></a>Interfaccia IDODownload

L'interfaccia **IDODownload** viene utilizzata per avviare e gestire un download.

## <a name="methods"></a>Metodi

L'interfaccia **IDODownload** dispone di questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDODownload:: Abort](./nf-do-idomanager-createdownload.md) | Interrompe il download. |
| [IDODownload:: Finalize](./nf-do-idodownload-finalize.md) | Completa il download. |
| [IDODownload:: GetProperty](./nf-do-idodownload-getproperty.md) | Recupera un puntatore a un **Variant** che contiene una specifica proprietà di download. |
| [IDODownload:: GetStatus](./nf-do-idodownload-getstatus.md) | Recupera un puntatore a una struttura **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Sospende il download. |
| [IDODownload:: SetProperty](./nf-do-idodownload-setproperty.md) | Imposta una proprietà di download. |
| [IDODownload:: Start](./nf-do-idodownload-start.md) | Avvia o riprende un download. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |