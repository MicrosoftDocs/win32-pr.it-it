---
description: Si sta provando a trovare altre informazioni sugli oggetti Direct3D durante il debug? Ad esempio, lo screenshot seguente mostra ciò che viene visualizzato in genere quando si esamina un'interfaccia Direct3D nella finestra espressioni di controllo.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Abilitazione di informazioni di debug Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123354"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Abilitazione di informazioni di debug Direct3D (Direct3D 9)

Si sta provando a trovare altre informazioni sugli oggetti Direct3D durante il debug? Ad esempio, lo screenshot seguente mostra ciò che viene visualizzato in genere quando si esamina un'interfaccia Direct3D nella finestra espressioni di controllo.

![Screenshot di un'interfaccia Direct3D nella finestra espressioni di controllo](images/d3d-debug-info1.png)

È possibile abilitare gli oggetti di debug di base in modo che un oggetto con mirroring che contiene tutte le proprietà dell'oggetto possa essere visualizzato nella finestra espressioni di controllo. È sufficiente includere i seguenti elementi \# define nel codice prima del file d3d9. h:


```
#define D3D_DEBUG_INFO
```



Per abilitare le informazioni di debug, è \# necessario compilare l'oggetto define prima del file d3d9. h (qualsiasi programma che usa DXUT consentirà automaticamente le \_ \_ informazioni di debug di D3D quando il programma viene compilato per il debug). Se si esegue un esempio di SDK, è possibile visualizzarlo in DXStdAfx. h, che ha effetto su tutti gli esempi di C++. È anche necessario eseguire debug Direct3D Runtime, che può essere abilitato dal pannello di controllo, se necessario.

Di seguito è riportato un esempio che usa l' [esempio BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Aggiungere la \# definizione al file Dxstdafx. h prima della riga 37.
2.  Compilare un progetto di debug.
3.  Impostare un punto di interruzione alla riga 307 in BasicHLSL. cpp
4.  Eseguire il debugger.

Lo screenshot seguente mostra il tipo di informazioni dettagliate che è possibile ottenere su un oggetto trama Direct3D dalla finestra espressioni di controllo.

![Screenshot di un oggetto trama Direct3D nella finestra espressioni di controllo](images/d3d-debug-info2.png)

> [!Note]
>
> I nomi delle proprietà dell'oggetto sono visibili e i valori sono corretti solo quando il runtime di debug è abilitato. Quando si esegue il runtime di vendita al dettaglio, i valori non sono validi.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Usare lo stack di chiamate per il debug esteso

Con il debug Direct3D abilitato, è anche possibile esaminare uno stack di chiamate ogni volta che viene creato un oggetto. Questa operazione renderà l'applicazione molto lenta, ma può essere usata per verificare la presenza di perdite di risorse. Per scrivere lo stack di chiamate, impostare la seguente chiave del registro di sistema su 1:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



La compilazione dell'applicazione con il debug abilitato consente di accedere a questa variabile aggiuntiva:


```
  LPCWSTR CreationCallStack;
```



Questa variabile archivia lo stack di chiamate ogni volta che viene creato un oggetto. Questa operazione renderà l'applicazione molto lenta, ma può essere usata per eseguire il debug delle perdite di risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 



