---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Rappresenta un dispositivo DirectML, utilizzato per creare operatori, associazioni di tabelle, registratori di comandi e altri oggetti.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: a23d6ec4299a2aa3ca7e9f6873167412d094af8d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320304"
---
# <a name="idmldevice1-interface-directmlh"></a>Interfaccia IDMLDevice1 (directml. h)

Rappresenta un dispositivo DirectML, utilizzato per creare operatori, associazioni di tabelle, registratori di comandi e altri oggetti. L'interfaccia **IDMLDevice1** eredita da [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).

Un dispositivo DirectML è sempre associato esattamente a un dispositivo Direct3D 12 sottostante. Tutti gli oggetti creati dal dispositivo DirectML gestiscono un riferimento sicuro al dispositivo padre. A differenza del dispositivo Direct3D 12, il dispositivo DML non è un singleton. È quindi possibile creare più dispositivi DirectML tramite lo stesso dispositivo Direct3D 12. Tuttavia, questa operazione non è consigliata perché il dispositivo DirectML non ha uno stato modificabile, quindi è possibile creare più dispositivi DML tramite lo stesso dispositivo Direct3D 12.

Questo oggetto è thread-safe.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Vedere anche [cronologia delle versioni di DirectML](../dml-version-history.md).

## <a name="availability"></a>Disponibilità
Questa API è stata introdotta nella versione DirectML `1.1.0` .

## <a name="tensor-constraints"></a>Vincoli tensore
**Piattaforma di destinazione**: Windows


## <a name="inheritance"></a>Ereditarietà


L'interfaccia IDMLDevice1 eredita dall'interfaccia IDMLDevice.



## <a name="methods"></a>Metodi

<p>L'interfaccia <b>IDMLDevice1</b> dispone di questi metodi.</p>

| Metodo | Descrizione |
| ---- |:---- |
| [IDMLDevice1::CompileGraph](../directml/nf-directml-idmldevice1-compilegraph.md) | Compila un grafico di operatori DirectML in un oggetto che può essere inviato alla GPU. |


## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | directml. h |

## <a name="see-also"></a>Vedi anche

[Interfaccia IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)