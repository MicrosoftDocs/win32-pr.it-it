---
description: 'Le applicazioni Direct3D possono essere eseguite in una delle due modalità seguenti: schermo intero o finestra.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Modalità finestra e Full-Screen predefinita (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a845c464e6c402c46cc4aff09196ccfde65ad90371187045b0c14c41315a9f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025751"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Modalità finestra e Full-Screen predefinita (Direct3D 9)

Le applicazioni Direct3D possono essere eseguite in una delle due modalità seguenti: schermo intero o finestra.

La modalità schermo intero indica che la finestra in cui viene eseguita l'applicazione copre l'intero desktop, nascondendo tutte le applicazioni in esecuzione (incluso l'ambiente di sviluppo). Per impostazione predefinita, i giochi sono in modalità schermo intero per coinvolgere completamente l'utente nel gioco nascondendo tutte le applicazioni in esecuzione. Un'applicazione in esecuzione in modalità finestra condivide il desktop con tutte le applicazioni in esecuzione. Le differenze di codice tra la modalità schermo intero e la modalità finestra sono molto piccole.

Poiché un'applicazione in esecuzione in modalità schermo intero assume il controllo dello schermo, il debug dell'applicazione richiede un monitoraggio separato o l'uso di un debugger remoto. Usare lo [strumento di Pannello di controllo DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) per abilitare il debug con più monitor. Uno dei vantaggi di un'applicazione in modalità finestra è che è possibile eseguire il codice un'istruzione alla volta in un debugger senza più monitor o un debugger remoto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 



