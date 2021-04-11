---
title: DirectComposition
description: In questo argomento viene illustrato lo scopo di Microsoft DirectComposition, vengono identificati i requisiti in fase di esecuzione e viene descritto lo sfondo di programmazione necessario per utilizzare Microsoft DirectComposition in modo efficace.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329180"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Scopo

Microsoft DirectComposition è un componente di Windows che consente la composizione di bitmap a prestazioni elevate con trasformazioni, effetti e animazioni. Gli sviluppatori di applicazioni possono usare l'API DirectComposition per creare interfacce utente visivamente accattivanti che presentano transizioni animate da un oggetto visivo all'altro fluide e ricche di funzionalità.

DirectComposition consente transizioni avanzate e fluide ottenendo un framerate elevato, usando hardware grafico e operando in modo indipendente dal thread dell'interfaccia utente. DirectComposition può accettare il contenuto bitmap disegnato da diverse librerie di rendering, incluse le bitmap Microsoft DirectX, e le bitmap sottoposte a rendering in una finestra (bitmap HWND). DirectComposition supporta inoltre un'ampia gamma di trasformazioni, come le trasformazioni affini 2D e le trasformazioni di prospettiva 3D, nonché gli effetti di base come il ritaglio e l'opacità.

DirectComposition è progettato per semplificare il processo di composizione di oggetti [*visivi*](directcomposition-glossary.md) e di creazione di transizioni animate. Se l'applicazione contiene già codice di rendering o usa già l'API DirectX consigliata, è sufficiente eseguire una quantità minima di lavoro per usare DirectComposition in modo efficace.

## <a name="developer-audience"></a>Sviluppatori

L'API DirectComposition è destinata a sviluppatori di grafica esperti e altamente idonei che conoscono C/C++, hanno una conoscenza approfondita del Component Object Model (COM) e hanno familiarità con i concetti di programmazione di Windows.

## <a name="run-time-requirements"></a>Requisiti di runtime

DirectComposition è stato introdotto in Windows 8. È incluso nelle piattaforme a 32 bit, a 64 e a ARM.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Perché usare DirectComposition?](why-use-directcomposition-.md)<br/>     | In questo argomento vengono descritte le funzionalità e i vantaggi di DirectComposition. <br/>                                                                           |
| [Come usare DirectComposition](how-to-use-directcomposition.md)<br/> | In questa sezione vengono descritte le procedure consigliate per l'utilizzo dell'API DirectComposition e viene illustrato come utilizzare l'API per eseguire diverse attività comuni. <br/> |
| [Concetti di DirectComposition](directcomposition-concepts.md)<br/>     | Questa sezione fornisce una panoramica concettuale di DirectComposition.<br/>                                                                                   |
| [Riferimento a DirectComposition](reference.md)<br/>                     | Questa sezione fornisce informazioni di riferimento dettagliate per gli elementi che costituiscono l'API DirectComposition.<br/>                                       |
| [Esempi di DirectComposition](directcomposition-code-samples.md)<br/>  | Le applicazioni di esempio seguenti illustrano come usare l'API DirectComposition e dimostrarne le funzionalità. <br/>                                      |
| [Glossario DirectComposition](directcomposition-glossary.md)<br/>     | In questo argomento vengono definiti i termini di DirectComposition. <br/>                                                                                                        |



 

 

 





