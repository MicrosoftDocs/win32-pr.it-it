---
title: Codici di errore in COM
description: Codici di errore in COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103959"
---
# <a name="error-codes-in-com"></a>Codici di errore in COM

Per indicare l'esito positivo o negativo, i metodi e le funzioni COM restituiscono un valore di tipo **HRESULT**. HRESULT **è** un intero a 32 bit. Il bit di ordine elevato di **HRESULT** segnala l'esito positivo o negativo. Zero (0) indica l'esito positivo e 1 indica un errore.

In questo modo vengono prodotti gli intervalli numerici seguenti:

-   Codici di esito positivo: 0x0-0x7FFFFFFF.
-   Codici di errore: 0x80000000-0xFFFFFFFF.

Un numero ridotto di metodi COM non restituisce un **valore HRESULT.** Ad esempio, i [**metodi AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**e Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) restituiscono valori long senza segno. Tuttavia, ogni metodo COM che restituisce un codice di errore restituisce un **valore HRESULT.**

Per verificare se un metodo COM ha esito positivo, esaminare il bit più alto **dell'HRESULT restituito.** Le Windows SDK le intestazioni forniscono due macro che semplificano questa operazione: la macro [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) e la macro [**FAILED.**](/windows/desktop/api/winerror/nf-winerror-failed) La macro **SUCCEEDED** restituisce **TRUE se** **un HRESULT** è un codice di esito positivo e **FALSE** se si tratta di un codice di errore. Nell'esempio seguente viene verificato se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ha esito positivo.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



A volte è più comodo testare la condizione inversa. La macro [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) esegue l'operazione opposta a [**SUCCEEDED.**](/windows/desktop/api/winerror/nf-winerror-succeeded) Restituisce **TRUE per** un codice di errore e **FALSE per** un codice di esito positivo.


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



Più avanti in questo modulo verranno visualizzati alcuni consigli pratici su come strutturare il codice per gestire gli errori COM. Vedere [Gestione degli errori in COM.](error-handling-in-com.md)

## <a name="next"></a>Prossima

[Creazione di un oggetto in COM](creating-an-object-in-com.md)

 

 
