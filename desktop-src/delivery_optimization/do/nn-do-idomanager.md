---
title: Interfaccia IDOManager
description: Utilizzato per creare un nuovo download e per enumerare i download esistenti.
keywords:
- Interfaccia IDOManager
topic_type:
- apiref
api_name:
- IDOManager
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a8755615e4d2f0fd074117438f8f305dce0cb681
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300306"
---
# <a name="idomanager-interface"></a>Interfaccia IDOManager

L'interfaccia **IDOManager** viene utilizzata per creare un nuovo download e per enumerare i download esistenti.

## <a name="methods"></a>Metodi

L'interfaccia **IDOManager** dispone di questi metodi.

| Metodo | Descrizione |
| ---- |:---- |
| [IDOManager::CreateDownload](./nf-do-idomanager-createdownload.md) | Crea un nuovo download. |
| [IDOManager::EnumDownloads](./nf-do-idomanager-enumdownloads.md) | Recupera un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i download esistenti. |

## <a name="requirements"></a>Requisiti

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Solo applicazioni Win32 Windows 10 versione 1809 \[\] |
| **Server minimo supportato** | Windows Server, \[ solo applicazioni Win32 versione 1809\] |
| **Intestazione** | Do. h |