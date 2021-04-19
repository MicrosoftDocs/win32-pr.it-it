---
description: Negoziazione di tipi di supporto
ms.assetid: 9872128c-4e3d-4ac8-afc4-b3dc516a0925
title: Negoziazione di tipi di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdcb78cfef6b8396d866ea148267c5a899cd353
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320805"
---
# <a name="negotiating-media-types"></a>Negoziazione di tipi di supporto

Quando il gestore del grafo del filtro chiama il metodo [**Ipin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) , dispone di diverse opzioni per specificare un tipo di supporto:

-   **Tipo completo:** Se il tipo di supporto è specificato completamente, i pin tentano di connettersi a tale tipo. In caso affermativo, il tentativo di connessione ha esito negativo.
-   **Tipo di supporto parziale:** Un tipo di supporto è *parziale* se il tipo principale, il sottotipo o il tipo di formato è \_ null GUID. Il valore \_ null GUID funge da "carattere jolly", che indica che qualsiasi valore è accettabile. I pin negoziano un tipo coerente con il tipo parziale.
-   **Nessun tipo di supporto:** Se il gestore del grafo del filtro passa un puntatore **null** , i pin possono accettare qualsiasi tipo di supporto accettabile per entrambi i pin.

Se i pin si connettono, la connessione ha sempre un tipo di supporto completo. Lo scopo del tipo di supporto fornito da Filter Graph Manager è limitare i tipi di connessione possibili.

Durante il processo di negoziazione, il pin di output propone un tipo di supporto chiamando il metodo [**Ipin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) del PIN di input. Il pin di input può accettare o rifiutare il tipo proposto. Questo processo si ripete fino a quando il pin di input non accetta un tipo o il pin di output esaurisce i tipi e la connessione ha esito negativo.

Il modo in cui un pin di output seleziona i tipi di supporto da proporre dipende dall'implementazione. Nelle classi base di DirectShow, il pin di output chiama [**Ipin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) sul pin di input. Questo metodo restituisce un enumeratore che enumera i tipi di supporti preferiti del PIN di input. In caso contrario, il pin di output enumera i propri tipi preferiti.

**Uso dei tipi di supporto**

In qualsiasi funzione che riceve un parametro del **\_ \_ tipo di supporto am** , convalidare sempre i valori di **cbFormat** e **formatType** prima di dereferenziare il membro **pbFormat** . Il codice seguente non è corretto:


```C++
if (pmt->formattype == FORMAT_VideoInfo)
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Wrong!
}
```



Il codice seguente è corretto:


```C++
if ((pmt->formattype == FORMAT_VideoInfo) && 
    (pmt->cbFormat > sizeof(VIDEOINFOHEADER) &&
    (pbFormat != NULL))
{
    VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    // Now you can dereference pVIH.
}
```



 

 



