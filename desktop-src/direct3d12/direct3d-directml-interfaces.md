---
title: Interfacce DirectML
description: Le interfacce seguenti sono dichiarate in DirectML.h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 64ae11c5b9a4298c340488499a5a309b71a2d48b
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521177"
---
# <a name="directml-interfaces"></a>Interfacce DirectML

Le interfacce seguenti sono dichiarate in DirectML.h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Registra le operazioni di directml in un elenco di comandi Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Rappresenta una forma compilata ed efficiente di un operatore adatto per l'esecuzione nella GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Controlla il livello di debug DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Rappresenta un dispositivo DirectML, utilizzato per creare operatori, tabelle di associazione, registratori di comandi e altri oggetti. |
| [**IDMLDevice1**](/windows/desktop/api/directml/nn-directml-idmldevice1) | Rappresenta un dispositivo DirectML, utilizzato per creare operatori, tabelle di associazione, registratori di comandi e altri oggetti. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Interfaccia implementata da tutti gli oggetti creati dal dispositivo DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implementato da oggetti che possono essere registrati in un elenco di comandi per l'invio nella GPU, usando [IDMLCommandRecorder::RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Interfaccia da cui [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) e [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) ereditano direttamente (e tutte le altre interfacce, indirettamente). Di conseguenza, fornisce metodi comuni a tutte le interfacce DirectML, in particolare i metodi per associare dati privati e per annotare i nomi degli oggetti. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Rappresenta un operatore DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Rappresenta un oggetto specializzato il cui scopo è inizializzare gli operatori compilati. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Implementato da oggetti che possono essere espulsi dalla memoria GPU e quindi che possono essere forniti a [IDMLDevice::Evict](/windows/desktop/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice::MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Argomenti correlati

* [Informazioni di riferimento su DirectML](direct3d-directml-reference.md)
* [Informazioni di riferimento di base](direct3d-12-core-reference.md)
* [Informazioni di riferimento su Direct3D 12](direct3d-12-reference.md)
