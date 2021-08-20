---
description: Stato del trasporto del dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Stato del trasporto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99ea7c3d6cba8363826c0fdab3cf411f0d68d6e284832a75c02cac3b1eefa770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952950"
---
# <a name="device-transport-state"></a>Stato del trasporto del dispositivo

Per recuperare lo stato corrente del dispositivo, ad esempio riproduzione, sospensione o arresto, chiamare il metodo [**IAMExtTransport::get \_ Mode.**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) Il metodo recupera una costante che indica lo stato del dispositivo:



| Valore                    | Stato dispositivo |
|--------------------------|--------------|
| RIPRODUZIONE \_ IN MODALITÀ \_ ED           | Esegui         |
| ARRESTO \_ DELLA MODALITÀ \_ ED           | Interrompere         |
| BLOCCO DELLA MODALITÀ ED \_ \_         | Sospendi        |
| MODALITÀ ED \_ \_ FF             | Avanzamento rapido |
| ED \_ MODE \_ REW            | Riavvolgimento rapido       |
| RECORD IN \_ MODALITÀ \_ ED         | Registra       |
| BLOCCO DEI \_ \_ RECORD IN MODALITÀ ED \_ | Sospendi record |



 

Il codice seguente controlla lo stato del dispositivo:


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



