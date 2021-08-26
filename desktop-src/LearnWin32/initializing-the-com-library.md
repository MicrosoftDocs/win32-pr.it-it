---
title: Inizializzazione della libreria COM
description: Inizializzazione della libreria COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1bc9536c186c2af3b604f7eb5666a6a31e7a845cf3b20f64a132119d16cb1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979991"
---
# <a name="initializing-the-com-library"></a>Inizializzazione della libreria COM

Qualsiasi Windows che usa COM deve inizializzare la libreria COM chiamando la [**funzione CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Ogni thread che usa un'interfaccia COM deve effettuare una chiamata separata a questa funzione. **CoInitializeEx** ha la firma seguente:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



Il primo parametro è riservato e deve essere **NULL.** Il secondo parametro specifica il modello di threading che verrà utilizzato dal programma. COM supporta due diversi modelli di threading, *apartment threaded* *e multithreading.* Se si specifica il threading apartment, si garantisce quanto segue:

-   Si accederà a ogni oggetto COM da un singolo thread. non si condivideranno puntatori a interfaccia COM tra più thread.
-   Il thread avrà un ciclo di messaggi. Vedere [Messaggi finestra](window-messages.md) nel modulo 1.

Se uno di questi vincoli non è true, usare il modello multithreading. Per specificare il modello di threading, impostare uno dei flag seguenti nel *parametro dwCoInit.*



| Flag                          | Descrizione         |
|-------------------------------|---------------------|
| **COINIT \_ APARTMENTTHREADED** | Apartment con thread. |
| **COINIT \_ MULTITHREADED**     | Multithreading.      |



 

È necessario impostare esattamente uno di questi flag. In genere, un thread che crea una finestra deve usare il flag **COINIT \_ APARTMENTTHREADED** e gli altri thread devono **usare COINIT \_ MULTITHREADED.** Tuttavia, alcuni componenti COM richiedono un particolare modello di threading. In tal caso, è consigliabile consultare la documentazione MSDN.

> [!Note]  
> In realtà, anche se si specifica il threading di apartment, è comunque possibile condividere le interfacce tra thread, usando una tecnica denominata *marshalling*. Il marshalling non è in ambito di questo modulo. Il punto importante è che con il threading di apartment, non è mai sufficiente copiare un puntatore a interfaccia in un altro thread. Per altre informazioni sui modelli di threading COM, vedere [Processi, thread e apartment.](/windows/desktop/com/processes--threads--and-apartments)

 

Oltre ai flag già menzionati, è buona idea impostare il flag **COINIT \_ DISABLE \_ OLE1DDE** nel *parametro dwCoInit.* L'impostazione di questo flag evita un sovraccarico associato a OLE (Object Linking and Embedding) 1.0, una tecnologia obsoleta.

Ecco come inizializzare COM per il threading di apartment:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



Il **tipo restituito HRESULT** contiene un codice di errore o di esito positivo. Nella sezione successiva verrà trattata la gestione degli errori COM.

## <a name="uninitializing-the-com-library"></a>Annullamento dell'inizializzazione della libreria COM

Per ogni chiamata riuscita a [**CoInitializeEx,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)è necessario chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) prima della chiusura del thread. Questa funzione non accetta parametri e non ha alcun valore restituito.


```C++
CoUninitialize();
```



## <a name="next"></a>Prossima

[Codici di errore in COM](error-codes-in-com.md)

 

 