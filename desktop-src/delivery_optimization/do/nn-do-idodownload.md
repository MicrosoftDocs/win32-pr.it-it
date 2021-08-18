---
title: Interfaccia IDODownload
description: Usato per avviare e gestire un download.
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
ms.openlocfilehash: 356d6ae2e01f91eae94d9d2ff01a39dd49708eb73a7287d8c176b4231654a74a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543818"
---
# <a name="idodownload-interface"></a>Interfaccia IDODownload

**L'interfaccia IDODownload** viene usata per avviare e gestire un download.

## <a name="methods"></a>Metodi

**L'interfaccia IDODownload** include questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDODownload::Abort](./nf-do-idomanager-createdownload.md) | Interrompe il download. |
| [IDODownload::Finalize](./nf-do-idodownload-finalize.md) | Finalizza il download. |
| [IDODownload::GetProperty](./nf-do-idodownload-getproperty.md) | Recupera un puntatore a un **variant che** contiene una proprietà di download specifica. |
| [IDODownload::GetStatus](./nf-do-idodownload-getstatus.md) | Recupera un puntatore a una **DO_DOWNLOAD_STATUS** che riflette lo stato corrente del download. |
| [IDODownload::P ause](./nf-do-idodownload-pause.md) | Sospende il download. |
| [IDODownload::SetProperty](./nf-do-idodownload-setproperty.md) | Imposta una proprietà di download. |
| [IDODownload::Start](./nf-do-idodownload-start.md) | Avvia o riprende un download. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | \[Windows 10, versione 1809 Solo applicazioni Win32\] |
| **Server minimo supportato** | Windows Server, solo applicazioni Win32 versione 1809 \[\] |
| **Intestazione** | Do.h |