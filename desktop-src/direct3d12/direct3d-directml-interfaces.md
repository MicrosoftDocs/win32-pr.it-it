---
title: Interfacce DirectML
description: Le interfacce seguenti sono dichiarate in DirectML. h.
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: 9752b52f1d9a311a1ada6b609a86691a336b77e7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "106300714"
---
# <a name="directml-interfaces"></a>Interfacce DirectML

Le interfacce seguenti sono dichiarate in DirectML. h.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) | Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12. |
| [**IDMLCommandRecorder**](/windows/desktop/api/directml/nn-directml-idmlcommandrecorder) | Registra il lavoro di DirectML in un elenco di comandi Direct3D 12. |
| [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) | Rappresenta una forma compilata ed efficiente di un operatore idoneo per l'esecuzione sulla GPU. |
| [**IDMLDebugDevice**](/windows/desktop/api/directml/nn-directml-idmldebugdevice) | Controlla il livello di debug di DirectML. |
| [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice) | Rappresenta un dispositivo DirectML, utilizzato per creare operatori, associazioni di tabelle, registratori di comandi e altri oggetti. |
| [**IDMLDevice1**](/windows/desktop/direct3d12/directml/nn-directml-idmldevice1) | Rappresenta un dispositivo DirectML, utilizzato per creare operatori, associazioni di tabelle, registratori di comandi e altri oggetti. |
| [**IDMLDeviceChild**](/windows/win32/api/directml/nn-directml-idmldevicechild) | Interfaccia implementata da tutti gli oggetti creati dal dispositivo DirectML. |
| [**IDMLDispatchable**](/windows/desktop/api/directml/nn-directml-idmldispatchable) | Implementata da oggetti che possono essere registrati in un elenco di comandi per la distribuzione sulla GPU, usando [IDMLCommandRecorder:: RecordDispatch](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch). |
| [**IDMLObject**](/windows/desktop/api/directml/nn-directml-idmlobject) | Interfaccia da cui [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice) e [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) ereditano direttamente (e tutte le altre interfacce indirettamente). Di conseguenza, fornisce i metodi comuni a tutte le interfacce DirectML, in particolare i metodi per associare i dati privati e annotare i nomi degli oggetti. |
| [**IDMLOperator**](/windows/desktop/api/directml/nn-directml-idmloperator) | Rappresenta un operatore DirectML. |
| [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) | Rappresenta un oggetto specializzato il cui scopo è quello di inizializzare gli operatori compilati. |
| [**IDMLPageable**](/windows/desktop/api/directml/nn-directml-idmlpageable) | Implementata da oggetti che possono essere rimossi dalla memoria GPU e che possono quindi essere forniti a [IDMLDevice:: Rimuovi](/windows/desktop/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice:: MakeResident](/windows/desktop/api/directml/nf-directml-idmldevice-makeresident). |

## <a name="related-topics"></a>Argomenti correlati

* [Riferimento a DirectML](direct3d-directml-reference.md)
* [Riferimento principale](direct3d-12-core-reference.md)
* [Guida di riferimento a Direct3D 12](direct3d-12-reference.md)
