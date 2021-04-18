---
description: Inizializza un oggetto servizio di sistema per installare un oggetto ActiveX quando l'utente corrente non dispone dell'autorizzazione per l'installazione dell'oggetto.
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
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315432"
---
# <a name="ieaxiservice-interface"></a>Interfaccia IeAxiService

L'interfaccia **IAxiService** Inizializza un oggetto servizio di sistema per installare un oggetto ActiveX quando l'utente corrente non dispone dell'autorizzazione per l'installazione dell'oggetto.

La classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa questa interfaccia.

Questa interfaccia non è dichiarata in un'intestazione pubblica. Le applicazioni devono definirle autonomamente. Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.

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

L'interfaccia **IeAxiService** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiService** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IeAxiService** dispone di questi metodi.



| Metodo                                        | Descrizione                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [**Pulizia**](ieaxiservice-cleanup.md)       | Libera le risorse usate dall'interfaccia **IeAxiService** .<br/> |
| [**Inizializzare**](ieaxiservice-initialize.md) | Verifica e Scarica un oggetto ActiveX.<br/>                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiService è definito come E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



 

