---
title: Direct Machine Learning (DirectML)
description: Direct Machine Learning (DirectML) è un'API di basso livello per Machine Learning. È dotata di un'interfaccia di programmazione familiare (C++ nativa, nano-COM) e di un flusso di lavoro nello stile di DirectX 12.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104323"
---
# <a name="direct-machine-learning-directml"></a>Direct Machine Learning (DirectML)

Direct Machine Learning (DirectML) è un'API di basso livello per Machine Learning. È dotata di un'interfaccia di programmazione familiare (C++ nativa, nano-COM) e di un flusso di lavoro nello stile di DirectX 12. È possibile integrare i carichi di lavoro del machine learning nel gioco, nel motore, nel middleware, nel back-end o in un'altra applicazione. DirectML è supportato da tutto l'hardware compatibile con DirectX 12.

DirectML è stato introdotto in Windows 10, versione 1903 e nella versione corrispondente del Windows SDK.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [Introduzione a DirectML](dml-intro.md) | Direct Machine Learning (DirectML) è un'API di basso livello per Machine Learning (ML). |
| [Binding in DirectML](dml-binding.md) | In DirectML, l' *associazione* si riferisce all'allegato di risorse alla pipeline per la GPU da usare durante l'inizializzazione e l'esecuzione degli operatori di machine learning. Queste risorse possono essere i tensori di input e di output, ad esempio, nonché le risorse temporanee o persistenti necessarie per l'operatore. |
| [Barriere UAV e barriere sullo stato delle risorse in DirectML](dml-barriers.md) | Vengono descritti i vantaggi di correttezza delle barriere e il modo in cui è possibile utilizzarli in DirectML. |
| [Uso di stride per esprimere il layout di riempimento e memoria](dml-strides.md) | I tensori DirectML sono descritti dalle proprietà note come *dimensioni* e dagli *stride* del tensore. |
| [Durata e sincronizzazione delle risorse](dml-resource-lifetime.md) | Per evitare un comportamento non definito, l'applicazione DirectML deve gestire correttamente le durate degli oggetti e la sincronizzazione tra la CPU e la GPU. |
| [Uso del livello di debug DirectML](dml-debug-layer.md) | Il livello di debug DirectML è un componente della fase di sviluppo facoltativo che consente di eseguire il debug del codice DirectML. |
| [Gestione degli errori e rimozione di dispositivi](dml-errors.md) | In questo argomento viene illustrato come eseguire il debug della rimozione del dispositivo DirectML e di altre condizioni di errore. |
| [Funzioni helper DirectML](dml-helper-functions.md) | Elenchi di codice delle funzioni di supporto DirectML essenziali. |
| [Applicazioni di esempio DirectML](dml-min-app.md) | Collegamenti alle applicazioni di esempio DirectML, incluso un esempio di un'applicazione DirectML minima. |

## <a name="related-topics"></a>Argomenti correlati

* [Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
