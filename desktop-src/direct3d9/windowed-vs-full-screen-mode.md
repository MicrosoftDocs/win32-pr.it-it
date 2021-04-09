---
description: 'Le applicazioni Direct3D possono essere eseguite in una delle due modalità seguenti: schermo intero o con finestra.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modalità di confronto Full-Screen finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123849"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Modalità di confronto Full-Screen finestra (Direct3D 9)

Le applicazioni Direct3D possono essere eseguite in una delle due modalità seguenti: schermo intero o con finestra.

La modalità schermo intero indica che la finestra in cui viene eseguita l'applicazione copre l'intero desktop, nascondendo tutte le applicazioni in esecuzione (incluso l'ambiente di sviluppo). Per impostazione predefinita, i giochi usano la modalità schermo intero per immergere completamente l'utente nel gioco nascondendo tutte le applicazioni in esecuzione. Un'applicazione in esecuzione in modalità Windows condivide il desktop con tutte le applicazioni in esecuzione. Le differenze di codice tra la modalità schermo intero e la modalità finestra sono molto ridotte.

Poiché un'applicazione in esecuzione in modalità schermo intero acquisisce lo schermo, il debug dell'applicazione richiede un monitoraggio separato o l'uso di un debugger remoto. Usare lo [strumento Pannello di controllo DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) per abilitare il debug di più monitor. Un vantaggio di un'applicazione in modalità finestra è che è possibile eseguire il codice un'istruzione alla volta in un debugger senza più monitoraggi o un debugger remoto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 



