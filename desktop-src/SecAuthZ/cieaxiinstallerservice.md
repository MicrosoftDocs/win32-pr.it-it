---
description: Implementa le interfacce IAxiService e IeAxiServiceCallback.
ms.assetid: 39f2ee3a-d4fd-4091-acd6-3d6b715bea75
title: Oggetto CIeAxiInstallerService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIeAxiInstallerService
api_type:
- COM
api_location: ''
ms.openlocfilehash: d8e96600762db414fa93316098d5ba87dabfbc3138f516d3d69f1740d0d33d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783087"
---
# <a name="cieaxiinstallerservice-object"></a>Oggetto CIeAxiInstallerService

**L'oggetto CIeAxiInstallerService** implementa le interfacce [**IAxiService**](ieaxiservice.md) e [**IeAxiServiceCallback.**](ieaxiservicecallback.md)

Questo oggetto non è dichiarato in un'intestazione pubblica. Le applicazioni devono definirlo in modo proprio. Il frammento IDL (Interface Definition Language) seguente descrive questo oggetto, incluso il relativo CLSID.

``` syntax
[
        uuid(90F18417-F0F1-484E-9D3C-59DCEEE5DBD8)
]
    coclass CIeAxiInstallerService
    {
        [default] interface IeAxiService;
        interface IeAxiServiceCallback;
    }

```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAxiService**](ieaxiservice.md)
</dt> <dt>

[**IeAxiServiceCallback**](ieaxiservicecallback.md)
</dt> </dl>

 

 




