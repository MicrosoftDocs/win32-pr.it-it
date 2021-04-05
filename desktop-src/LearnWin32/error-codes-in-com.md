---
title: Codici di errore in COM
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725386"
---
# <a name="error-codes-in-com"></a>Codici di errore in COM

Per indicare l'esito positivo o negativo, i metodi e le funzioni COM restituiscono un valore di tipo **HRESULT**. **HRESULT** è un valore integer a 32 bit. Il bit più significativo del valore **HRESULT** segnala l'esito positivo o negativo. Zero (0) indica esito positivo e 1 indica un errore.

Producendo gli intervalli numerici seguenti:

-   Codici di esito positivo: 0x0 – 0x7FFFFFFF.
-   Codici di errore: 0x80000000 – 0xFFFFFFFF.

Un numero ridotto di metodi COM non restituisce un valore **HRESULT** . Ad esempio, i metodi [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) restituiscono valori long senza segno. Tuttavia, ogni metodo COM che restituisce un codice di errore esegue questa operazione restituendo un valore **HRESULT** .

Per controllare se un metodo COM ha esito positivo, esaminare il bit più significativo dell' **HRESULT** restituito. Le intestazioni Windows SDK forniscono due macro che semplificano questa operazione, ovvero la macro [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded) e la macro [**non riuscita**](/windows/desktop/api/winerror/nf-winerror-failed) . La macro **succeeded** restituisce **true** se un **HRESULT** è un codice di esito positivo e **false** se è un codice di errore. Nell'esempio seguente viene verificato se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) ha esito positivo.


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



A volte è più pratico testare la condizione inversa. La macro non [**riuscita**](/windows/desktop/api/winerror/nf-winerror-failed) esegue l'operazione opposta rispetto a [**succeeded**](/windows/desktop/api/winerror/nf-winerror-succeeded). Restituisce **true** per un codice di errore e **false** per un codice di esito positivo.


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



Più avanti in questo modulo, si esamineranno alcuni consigli pratici su come strutturare il codice per gestire gli errori COM. Vedere [gestione degli errori in com](error-handling-in-com.md).

## <a name="next"></a>Prossima

[Creazione di un oggetto in COM](creating-an-object-in-com.md)

 

 