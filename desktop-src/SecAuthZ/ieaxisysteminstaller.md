---
description: Installa un oggetto ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interfaccia IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058135"
---
# <a name="ieaxisysteminstaller-interface"></a>Interfaccia IeAxiSystemInstaller

L'interfaccia **IeAxiSystemInstaller** installa un oggetto ActiveX.

Questa interfaccia non è dichiarata in un'intestazione pubblica. Le applicazioni devono definirle autonomamente. Il frammento IDL (Interface Definition Language) seguente descrive questa interfaccia, incluso il relativo IID.

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a>Membri

L'interfaccia **IeAxiSystemInstaller** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IeAxiSystemInstaller** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IeAxiSystemInstaller** dispone di questi metodi.



| Metodo                                                                              | Descrizione                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [**InitializeSystemInstaller**](ieaxisysteminstaller-initializesysteminstaller.md) | Installa l'oggetto ActiveX specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                 |
| IID<br/>                      | IID \_ IeAxiSystemInstaller è definito come a50ea6f8-4764-4299-B309-022b2a8b4d8d<br/>                   |



 

