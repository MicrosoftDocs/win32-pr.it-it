---
description: Stato del trasporto del dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Stato del trasporto del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401346"
---
# <a name="device-transport-state"></a>Stato del trasporto del dispositivo

Per recuperare lo stato corrente del dispositivo, ad esempio Play, pause o stop, chiamare il metodo [**IAMExtTransport:: Get \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) . Il metodo recupera una costante che indica lo stato del dispositivo:



| Valore                    | Stato dispositivo |
|--------------------------|--------------|
| \_riproduzione in modalità ed \_           | Esegui         |
| \_arresto modalità \_ ed           | Interrompere         |
| \_Blocca modalità \_ ed         | Sospendi        |
| \_modalità ed \_ FF             | Avanzamento rapido |
| \_modalità ed \_ r            | Riavvolgimento rapido       |
| \_record in modalità ed \_         | Registra       |
| \_blocco del \_ record in modalità ed \_ | Registrare-sospendere |



 

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

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



