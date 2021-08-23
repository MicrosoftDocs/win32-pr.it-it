---
title: Interfacce DirectML
description: Le interfacce seguenti vengono dichiarate in DirectML.h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: deb388962043926afd3868785364df6297b05d78f3997359fc88ea97ab679f33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728951"
---
# <a name="directml-interfaces"></a>Interfacce DirectML

Le interfacce seguenti vengono dichiarate in DirectML.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Registra le operazioni di invio di DirectML in un elenco di comandi Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Rappresenta una forma compilata ed efficiente di un operatore adatto per l'esecuzione nella GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Controlla il livello di debug DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Rappresenta un dispositivo DirectML, utilizzato per creare operatori, tabelle di associazione, registratori di comandi e altri oggetti. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Rappresenta un dispositivo DirectML, utilizzato per creare operatori, tabelle di associazione, registratori di comandi e altri oggetti. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Interfaccia implementata da tutti gli oggetti creati dal dispositivo DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implementato da oggetti che possono essere registrati in un elenco di comandi per l'invio nella GPU, usando [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Interfaccia da cui [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) e [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) ereditano direttamente (e indirettamente tutte le altre interfacce). Di conseguenza, fornisce metodi comuni a tutte le interfacce DirectML, in particolare metodi per associare dati privati e annotare i nomi degli oggetti. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Rappresenta un operatore DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Rappresenta un oggetto specializzato il cui scopo è inizializzare gli operatori compilati. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Implementato da oggetti che possono essere espulsi dalla memoria GPU e che possono quindi essere forniti a [IDMLDevice::Evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice::MakeResident.](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident) |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento su DirectML](direct3d-directml-reference.md)
* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
