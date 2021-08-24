---
description: Chiamato dall'interfaccia IeAxiSystemInstaller per verificare che sia ActiveX un oggetto .
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
ms.openlocfilehash: 3313a1744a1fb9a3b34549ca32bb9b0c7cf18977c7785075900c4a11425b5949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908351"
---
# <a name="ieaxiservicecallback-interface"></a>Interfaccia IeAxiServiceCallback

**L'interfaccia IeAxiServiceCallback** viene chiamata dall'interfaccia [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) per verificare che sia possibile ActiveX'oggetto .

La [**classe CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa questa interfaccia.

Questa interfaccia non è dichiarata in un'intestazione pubblica. Le applicazioni devono definirlo in modo proprio. Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.

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

**L'interfaccia IeAxiServiceCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiServiceCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IeAxiServiceCallback** include questi metodi.



| Metodo                                                | Descrizione                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**VerifyFile**](ieaxiservicecallback-verifyfile.md) | Esegue controlli di sicurezza sull'oggetto ActiveX specificato e restituisce il percorso in cui è stato scaricato il file .cab corrispondente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiServiceCallback è definito come 1823E7BA-EC36-447a-9B2E-B4912E15AFE7<br/>                   |



 

