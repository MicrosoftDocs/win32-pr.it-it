---
title: Attributi direzionali (parametro)
description: Gli attributi direzionali descrivono se i dati vengono trasmessi da client a server, da server a client o da entrambi.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- RPC Remote Procedure Call , descritto, attributi direzionali
- in
- in uscita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e9ff23e7e12acbd5cf301afe6786599268d2e149878a326a62f79cd91f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930665"
---
# <a name="directional-parameter-attributes"></a>Attributi direzionali (parametro)

Gli attributi direzionali descrivono se i dati vengono trasmessi da client a server, da server a client o da entrambi. Tutti i parametri nel prototipo di funzione devono essere associati ad attributi direzionali. Le tre possibili combinazioni di attributi direzionali sono: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] e 3) \[ **in**, **out** \] . Questi descrivono il modo in cui i parametri vengono passati tra le routine chiamanti e chiamate. Quando si esegue la compilazione nell'impostazione predefinita (modalità estesa Microsoft) e si omette un attributo direzionale per un parametro, il compilatore MIDL presuppone il valore predefinito \[ **in** \] .

Un \[ [**parametro out**](/windows/desktop/Midl/out-idl) \] deve essere un puntatore. In realtà, \[ **l'attributo out** non è significativo se applicato a parametri che non fungono da puntatori perché i parametri della funzione \] C vengono passati per valore. In C la funzione chiamata riceve una copia privata del valore del parametro. non può modificare il valore della funzione chiamante per tale parametro. Se tuttavia il parametro funge da puntatore, può essere usato per accedere alla memoria e modificarla. L'attributo out indica che la funzione server deve restituire il valore alla funzione chiamante del client e che la memoria associata al puntatore deve essere restituita in base agli attributi assegnati al \[  \] puntatore.

L'interfaccia seguente illustra le tre possibili combinazioni di attributi direzionali che possono essere applicati a un parametro. La funzione **InOutProc** è definita nel file IDL come:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

Il primo parametro, *s1,* è \[ [**solo in**](/windows/desktop/Midl/in) \] . Il valore viene trasmesso al computer remoto, ma non viene restituito alla procedura chiamante. Anche se l'applicazione server può modificare il valore per *s1*, il valore di *s1* nel client è lo stesso prima e dopo la chiamata.

Il secondo parametro, *ps2*, è definito nel prototipo di funzione come puntatore con attributi \[ [**in**](/windows/desktop/Midl/in) \] e \[ [](/windows/desktop/Midl/out-idl) \] out. \[ **L'attributo** \] in indica che il valore del parametro viene passato dal client al server. \[ **L'attributo out** \] indica che il valore a cui punta *ps2* viene restituito al client.

Il terzo parametro è \[ [**out**](/windows/desktop/Midl/out-idl) \] only. Lo spazio viene allocato per il parametro nel server, ma il valore non è definito alla voce. Come accennato in \[ **precedenza, tutti i** parametri out \] devono essere puntatori.

La procedura remota modifica il valore di tutti e tre i parametri, ma solo i nuovi valori dei parametri out e \[ [](/windows/desktop/Midl/out-idl) \] \[ [**in**](/windows/desktop/Midl/in) \] sono disponibili per il client.


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



Al ritorno dalla chiamata a **InOutProc,** il secondo e il terzo parametro vengono modificati. Il primo parametro, che è \[ [**solo in**](/windows/desktop/Midl/in) \] , rimane invariato.

![parametri in](images/prog-a22.png)

![out (parametri)](images/prog-a23.png)

![parametri in-out](images/prog-a21.png)

 

 