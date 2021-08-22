---
title: DirectComposition
description: Questo argomento illustra lo scopo di Microsoft DirectComposition, ne identifica i requisiti in fase di esecuzione e descrive il background di programmazione necessario per usare Microsoft DirectComposition in modo efficace.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- DirectComposition API
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca1b13dbd0ee4893f1b208cd88d7fd1251b5fb7ece2400b7e0b195e84865b2d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985411"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> Per le app Windows 10, è consigliabile usare le API Windows.UI.Composition anziché DirectComposition. Per altre informazioni, vedere [Modernizzare l'app desktop usando il livello Visivo.](/windows/uwp/composition/visual-layer-in-desktop-apps)

## <a name="purpose"></a>Scopo

Microsoft DirectComposition è un Windows che consente la composizione bitmap ad alte prestazioni con trasformazioni, effetti e animazioni. Gli sviluppatori di applicazioni possono usare l'API DirectComposition per creare interfacce utente visivamente accattivanti che presentano transizioni animate da un oggetto visivo all'altro fluide e ricche di funzionalità.

DirectComposition consente transizioni ricche e fluide ottenendo un framerate elevato, usando hardware grafico e operando indipendentemente dal thread dell'interfaccia utente. DirectComposition può accettare contenuto bitmap disegnato da librerie di rendering diverse, tra cui bitmap Microsoft DirectX e bitmap sottoposte a rendering in una finestra (bitmap HWND). DirectComposition supporta anche un'ampia gamma di trasformazioni, ad esempio trasformazioni affine 2D e trasformazioni di prospettiva 3D, nonché effetti di base come ritaglio e opacità.

DirectComposition è progettato per semplificare il processo di composizione [*di oggetti visivi*](directcomposition-glossary.md) e creazione di transizioni animate. Se l'applicazione contiene già codice di rendering o usa già l'API DirectX consigliata, è necessario eseguire solo una quantità minima di lavoro per usare DirectComposition in modo efficace.

## <a name="developer-audience"></a>Sviluppatori

L'API DirectComposition è destinata agli sviluppatori di grafica esperti e altamente idonei che conoscono C/C++, hanno una conoscenza approfondita di Component Object Model (COM) e hanno familiarità con i concetti di programmazione Windows.

## <a name="run-time-requirements"></a>Requisiti di runtime

DirectComposition è stato introdotto in Windows 8. È incluso nelle piattaforme ARM, a 32 bit e a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                       | Descrizione                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Perché usare DirectComposition?](why-use-directcomposition-.md)<br/>     | Questo argomento descrive le funzionalità e i vantaggi di DirectComposition. <br/>                                                                           |
| [Come usare DirectComposition](how-to-use-directcomposition.md)<br/> | Questa sezione descrive le procedure consigliate per l'uso dell'API DirectComposition e illustra come usare l'API per eseguire diverse attività comuni. <br/> |
| [Concetti relativi a DirectComposition](directcomposition-concepts.md)<br/>     | Questa sezione offre una panoramica concettuale di DirectComposition.<br/>                                                                                   |
| [Informazioni di riferimento su DirectComposition](reference.md)<br/>                     | Questa sezione fornisce informazioni di riferimento dettagliate per gli elementi che costituiscono l'API DirectComposition.<br/>                                       |
| [Esempi di DirectComposition](directcomposition-code-samples.md)<br/>  | Le applicazioni di esempio seguenti illustrano come usare l'API DirectComposition e illustrarne le funzionalità. <br/>                                      |
| [Glossario di DirectComposition](directcomposition-glossary.md)<br/>     | Questo argomento definisce i termini di DirectComposition. <br/>                                                                                                        |



 

 

 





