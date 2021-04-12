---
title: Uso di interfacce con il controllo Media Player di Windows
description: Uso di interfacce con il controllo Media Player di Windows
ms.assetid: 0381e0e4-c686-4ab4-b947-b883b6f4e06e
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, C++
- Modello a oggetti di Windows Media Player, C++
- modello a oggetti, C++
- Windows Media Player Mobile, C++
- Controllo ActiveX di Windows Media Player, C++
- Controllo ActiveX Windows Media Player Mobile, C++
- Controllo ActiveX, C++
- Incorporamento del programma C++
- incorporamento, programmi C++
- Controllo ActiveX di Windows Media Player, interfacce
- Controllo ActiveX Windows Media Player Mobile, interfacce
- Controllo ActiveX, interfacce
- interfacce, incorporamento del controllo ActiveX
- Windows Media Player Skin, incorporamento del controllo ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714a8be9e471541d008fcb76a4b0398dba2162b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221467"
---
# <a name="using-skins-with-the-windows-media-player-control"></a>Uso di interfacce con il controllo Media Player di Windows

Quando si incorpora il controllo Media Player di Windows in un programma C++, è possibile personalizzare l'interfaccia utente del lettore applicando un file di definizione dell'interfaccia personalizzata. Un file di definizione dell'interfaccia è un documento basato su XML che specifica il layout dei componenti dell'interfaccia utente standard e personalizzabili e di qualsiasi grafica associata. Utilizzando Microsoft JScript, è possibile specificare il comportamento di questi componenti e modificare il controllo Media Player Windows senza l'overhead della sintassi C++ e COM.

Le interfacce forniscono un modo semplice per mantenere il codice dell'interfaccia utente e il codice del programma principale separatamente, in modo che possano essere mantenuti e sviluppati in modo indipendente. È anche possibile riutilizzare le interfacce originariamente progettate per l'uso da parte del lettore autonomo in modalità Skin. Il codice di interfaccia progettato in modo specifico per i programmi C++ può interagire con i programmi tramite un oggetto che può essere fornito dal programma tramite script.

Per abilitare la modalità Skin per il controllo Media Player di Windows, è necessario che il programma implementi l'interfaccia **IWMPRemoteMediaServices** . Sebbene sia possibile usare le interfacce con il controllo e il controllo in remoto contemporaneamente, è possibile usare questa interfaccia per abilitare le funzionalità senza abilitare l'altra. Per disabilitare la comunicazione remota, è sufficiente passare un valore di "local" come parametro out del metodo **GetServiceType** e restituire un valore HRESULT di e \_ NOTIMPL dal metodo **getApplicationName** .

Per passare il controllo Media Player di Windows alla modalità interfaccia personalizzata, chiamare il metodo **IWMPPlayer::p UT \_ uiMode** , passando il valore "Custom". Specificare il percorso e il nome file del file di definizione Skin da usare restituendo il percorso dal metodo **IWMPRemoteMediaServices:: GetCustomUIMode** .

Se si vuole fornire un oggetto tramite script per la comunicazione tra l'interfaccia utente e il programma, passare un nome e un puntatore a un puntatore **IDispatch** come due parametri out del metodo **IWMPRemoteMediaServices:: GetScriptableObject** . L'interfaccia può quindi effettuare chiamate all'oggetto gestibile tramite script usando il nome specificato come se fosse un attributo globale simile all'attributo globale **Player** .

Un'interfaccia applicata a un controllo Media Player Windows remoto può accedere all'oggetto **PlayerApplication** usando un altro attributo globale denominato **PlayerApplication**. Poiché non è possibile accedere alla proprietà **Player. playerApplication** tramite interfacce, è necessario usare questo attributo globale quando si vuole che il codice dell'interfaccia utente gestisca l'ancoraggio e la disancoraggio.

## <a name="samples"></a>Esempi

Il pacchetto di installazione di Windows Media Player SDK installa un esempio che illustra l'applicazione di un'interfaccia al controllo Media Player di Windows. Per ulteriori informazioni, vedere l'esempio RemoteSkin.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempi**](samples.md)
</dt> <dt>

[**Uso del controllo Media Player di Windows in un programma C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




