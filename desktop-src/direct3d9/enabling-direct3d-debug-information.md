---
description: Si stanno tentando di trovare altre informazioni sugli oggetti Direct3D durante il debug? Ad esempio, lo screenshot seguente mostra ciò che si vede in genere quando si osserva un'interfaccia Direct3D nella finestra Espressioni di controllo.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Abilitazione delle informazioni di debug Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88851c144c2e651e920d870618f66a38028207bc5503f513f45fb053e16bd2e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730164"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Abilitazione delle informazioni di debug Direct3D (Direct3D 9)

Si stanno tentando di trovare altre informazioni sugli oggetti Direct3D durante il debug? Ad esempio, lo screenshot seguente mostra ciò che si vede in genere quando si osserva un'interfaccia Direct3D nella finestra Espressioni di controllo.

![Screenshot di un'interfaccia direct3d nella finestra Espressioni di controllo](images/d3d-debug-info1.png)

È possibile abilitare gli oggetti di debug principali in modo che un oggetto con mirroring che contiene tutte le proprietà dell'oggetto possa essere visualizzato nella finestra Espressioni di controllo. È sufficiente includere la \# definizione seguente nel codice prima del file D3D9.h:


```
#define D3D_DEBUG_INFO
```



Per abilitare le informazioni di debug, la definizione deve essere compilata prima del \# file D3D9.h (qualsiasi programma che usa DXUT abiliterà automaticamente LE INFORMAZIONI DI DEBUG D3D quando il programma viene compilato per il \_ \_ debug). Se si esegue un esempio sdk, è possibile vedere questo in DXStdAfx.h (che influisce su tutti gli esempi C++). È anche necessario eseguire il runtime Direct3D di debug (che può essere abilitato dal Pannello di controllo se necessario).

Di seguito è riportato un esempio che usa [l'esempio BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Aggiungere la \# definizione al file Dxstdafx.h prima della riga 37.
2.  Compilare un progetto di debug.
3.  Impostare un punto di interruzione alla riga 307 in BasicHLSL.cpp
4.  Eseguire il debugger.

Lo screenshot seguente mostra il tipo di informazioni dettagliate che è possibile ottenere su un oggetto trama Direct3D dalla finestra Espressioni di controllo.

![Screenshot di un oggetto trama direct3d nella finestra Espressioni di controllo](images/d3d-debug-info2.png)

> [!Note]
>
> I nomi delle proprietà dell'oggetto sono visibili e i valori sono corretti solo quando è abilitato il runtime di debug. Durante l'esecuzione nel runtime di vendita al dettaglio, i valori non sono validi.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Usare lo stack di chiamate per il debug esteso

Con il debug Direct3D abilitato, è anche possibile esaminare uno stack di chiamate ogni volta che viene creato un oggetto. In questo modo l'applicazione sarà molto lenta, ma può essere usata per verificare la presenza di perdite di risorse. Per scrivere lo stack di chiamate, impostare la chiave del Registro di sistema seguente su 1:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



La compilazione dell'applicazione con il debug abilitato consente di accedere a questa variabile aggiuntiva:


```
  LPCWSTR CreationCallStack;
```



Questa variabile archivierà lo stack di chiamate ogni volta che viene creato un oggetto. In questo modo l'applicazione sarà molto lenta, ma può essere usata per eseguire il debug delle perdite di risorse.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 



