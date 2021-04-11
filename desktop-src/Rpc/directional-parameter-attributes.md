---
title: Attributi direzionali (parametro)
description: Gli attributi direzionali descrivono se i dati vengono trasmessi da client a server, da server a client o da entrambi.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- RPC (Remote Procedure Call), descritti, attributi direzionali
- in ingresso
- in uscita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118099"
---
# <a name="directional-parameter-attributes"></a>Attributi direzionali (parametro)

Gli attributi direzionali descrivono se i dati vengono trasmessi da client a server, da server a client o da entrambi. Tutti i parametri nel prototipo di funzione devono essere associati a attributi direzionali. Le tre possibili combinazioni di attributi direzionali sono: 1) \[ [**in**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] e 3) \[ **in**, **out** \] . Che descrivono il modo in cui i parametri vengono passati tra la chiamata e le routine chiamate. Quando si compila nell'impostazione predefinita (modalità estesa Microsoft) e si omette un attributo direzionale per un parametro, il compilatore MIDL presuppone che il valore predefinito sia \[ **in** \] .

Un \[ parametro [**out**](/windows/desktop/Midl/out-idl) \] deve essere un puntatore. Infatti, l'attributo \[ **out** \] non è significativo quando viene applicato a parametri che non fungono da puntatori perché i parametri della funzione C vengono passati per valore. In C, la funzione chiamata riceve una copia privata del valore del parametro. non può modificare il valore della funzione chiamante per il parametro. Tuttavia, se il parametro funge da puntatore, può essere utilizzato per accedere e modificare la memoria. L' \[  \] attributo out indica che la funzione server deve restituire il valore alla funzione chiamante del client e che la memoria associata al puntatore deve essere restituita secondo gli attributi assegnati al puntatore.

Nell'interfaccia seguente vengono illustrate le tre possibili combinazioni di attributi direzionali che è possibile applicare a un parametro. La funzione **InOutProc** è definita nel file IDL come:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

Il primo parametro, *S1*, è \[ solo [**in**](/windows/desktop/Midl/in) \] . Il relativo valore viene trasmesso al computer remoto, ma non viene restituito alla procedura chiamante. Sebbene l'applicazione server possa modificare il proprio valore per *S1*, il valore di *S1* sul client è lo stesso prima e dopo la chiamata.

Il secondo parametro, *PS2*, viene definito nel prototipo di funzione come puntatore con \[ [](/windows/desktop/Midl/in) \] gli attributi in e \[ [**out**](/windows/desktop/Midl/out-idl) \] . L' \[ attributo **in** \] indica che il valore del parametro viene passato dal client al server. L' \[  \] attributo out indica che al client viene restituito il valore a cui punta *PS2* .

Il terzo parametro è \[ [**out**](/windows/desktop/Midl/out-idl) \] only. Lo spazio viene allocato per il parametro sul server, ma il valore non è definito alla voce. Come indicato in precedenza, tutti i \[ parametri **out** \] devono essere puntatori.

La procedura remota modifica il valore di tutti e tre i parametri, ma solo i nuovi valori dei \[ [](/windows/desktop/Midl/out-idl) \] parametri out e \[ [**in**](/windows/desktop/Midl/in) \] sono disponibili per il client.


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



Al ritorno dalla chiamata a **InOutProc**, il secondo e il terzo parametro vengono modificati. Il primo parametro, che è \[ solo [**in**](/windows/desktop/Midl/in) \] , è invariato.

![parametri in](images/prog-a22.png)

![out (parametri)](images/prog-a23.png)

![parametri in uscita](images/prog-a21.png)

 

 