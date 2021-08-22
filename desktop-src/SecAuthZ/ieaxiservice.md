---
description: Inizializza un oggetto servizio di sistema per installare un ActiveX quando l'utente corrente non dispone dell'autorizzazione per installare l'oggetto.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interfaccia IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: f799b0b306d10e8246afbef83e4677729f6a735a52e5e4ed4954b873ec5b6201
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119414721"
---
# <a name="ieaxiservice-interface"></a>Interfaccia IeAxiService

**L'interfaccia IAxiService** inizializza un oggetto servizio di sistema per installare un oggetto ActiveX quando l'utente corrente non dispone dell'autorizzazione per installare l'oggetto.

La [**classe CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa questa interfaccia.

Questa interfaccia non è dichiarata in un'intestazione pubblica. Le applicazioni devono definirlo in modo proprio. Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a>Membri

**L'interfaccia IeAxiService** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IeAxiService** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IeAxiService** include questi metodi.



| Metodo                                        | Descrizione                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Pulitura**](ieaxiservice-cleanup.md)       | Libera le risorse usate **dall'interfaccia IeAxiService.**<br/> |
| [**Inizializzare**](ieaxiservice-initialize.md) | Controlla e scarica un oggetto ActiveX.<br/>                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows solo app desktop Vista Ultimate \[\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService è definito come E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 

