---
title: Inizializzazione della libreria COM
description: Inizializzazione della libreria COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299782"
---
# <a name="initializing-the-com-library"></a>Inizializzazione della libreria COM

Qualsiasi programma Windows che usa COM deve inizializzare la libreria COM chiamando la funzione [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) . Ogni thread che usa un'interfaccia COM deve effettuare una chiamata separata a questa funzione. **CoInitializeEx** ha la firma seguente:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



Il primo parametro è riservato e deve essere **null**. Il secondo parametro specifica il modello di threading che il programma utilizzerà. COM supporta due modelli di threading diversi, con *Threading di Apartment* e *multithreading*. Se si specifica il threading dell'Apartment, si apportano le garanzie seguenti:

-   Ogni oggetto COM sarà accessibile da un singolo thread. i puntatori di interfaccia COM non vengono condivisi tra più thread.
-   Il thread avrà un ciclo di messaggi. (Vedere [messaggi della finestra](window-messages.md) nel modulo 1).

Se uno di questi vincoli non è true, utilizzare il modello multithread. Per specificare il modello di threading, impostare uno dei flag seguenti nel parametro *dwCoInit* .



| Flag                          | Descrizione         |
|-------------------------------|---------------------|
| **CoInit \_ ApartmentThreaded** | Threading Apartment. |
| **CoInit \_ MULTIthreading**     | Multithreading.      |



 

È necessario impostare esattamente uno di questi flag. In genere, un thread che crea una finestra deve usare il flag **CoInit \_ ApartmentThreaded** e gli altri thread usano il **\_ multithreading di CoInit**. Tuttavia, alcuni componenti COM richiedono un particolare modello di Threading. La documentazione di MSDN dovrebbe indicare quando questo è il caso.

> [!Note]  
> In realtà, anche se si specifica il threading dell'Apartment, è comunque possibile condividere le interfacce tra i thread, usando una tecnica chiamata *marshalling*. Il marshalling esula dall'ambito di questo modulo. Il punto importante è che, con il threading dell'Apartment, non è mai sufficiente copiare un puntatore di interfaccia in un altro thread. Per ulteriori informazioni sui modelli di threading COM, vedere [processi, thread e Apartment](/windows/desktop/com/processes--threads--and-apartments).

 

Oltre ai flag già citati, è consigliabile impostare il flag **CoInit \_ Disable \_ OLE1DDE** nel parametro *dwCoInit* . L'impostazione di questo flag evita un sovraccarico associato a Object Linking and Embedding (OLE) 1,0, una tecnologia obsoleta.

Di seguito viene illustrato come inizializzare COM per il threading di Apartment:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



Il tipo restituito **HRESULT** contiene un errore o un codice di esito positivo. Nella sezione successiva verrà esaminata la gestione degli errori COM.

## <a name="uninitializing-the-com-library"></a>Annullamento dell'inizializzazione della libreria COM

Per ogni chiamata riuscita a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), è necessario chiamare [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) prima che il thread venga chiuso. Questa funzione non accetta parametri e non restituisce alcun valore.


```C++
CoUninitialize();
```



## <a name="next"></a>Prossima

[Codici di errore in COM](error-codes-in-com.md)

 

 