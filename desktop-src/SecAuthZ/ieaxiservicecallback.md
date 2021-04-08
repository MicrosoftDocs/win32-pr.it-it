---
description: Chiamato dall'interfaccia IeAxiSystemInstaller per verificare che sia possibile installare un oggetto ActiveX.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interfaccia IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885669"
---
# <a name="ieaxiservicecallback-interface"></a>Interfaccia IeAxiServiceCallback

L'interfaccia **IeAxiServiceCallback** viene chiamata dall'interfaccia [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) per verificare che sia possibile installare un oggetto ActiveX.

La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa questa interfaccia.

Questa interfaccia non è dichiarata in un'intestazione pubblica. Le applicazioni devono definirle autonomamente. Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a>Membri

L'interfaccia **IeAxiServiceCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiServiceCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IeAxiServiceCallback** dispone di questi metodi.



| Metodo                                                | Descrizione                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | Esegue i controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file con estensione CAB corrispondente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback è definito come 1823E7BA-EC36-447A-9B2E-B4912E15AFE7<br/>                   |



 

