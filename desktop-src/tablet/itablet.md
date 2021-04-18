---
description: Rappresenta un tablet collegato al computer.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interfaccia ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314916"
---
# <a name="itablet-interface"></a>Interfaccia ITablet

Rappresenta un tablet collegato al computer.

## <a name="members"></a>Membri

L'interfaccia **ITablet** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITablet** dispone di questi metodi.



| Metodo                                                                 | Descrizione                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateContext**](itablet-createcontext.md)                         | Crea un oggetto di contesto che descrive il dispositivo Tablet specificato.<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | Recupera l'oggetto [**ITabletCursor**](itabletcursor.md) specificato.<br/>     |
| [**GetCursorCount**](itablet-getcursorcount.md)                       | Recupera il numero di oggetti cursori associati al tablet.<br/>         |
| [**GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md) | Recupera le impostazioni di contesto predefinite per il tablet.<br/>                     |
| [**GetHardwareCaps**](itablet-gethardwarecaps.md)                     | Recupera un valore che rappresenta le funzionalità dell'hardware del tablet.<br/> |
| [**GetMaxInputRect**](itablet-getmaxinputrect.md)                     | Recupera un rettangolo che rappresenta l'area di input massima della tavoletta.<br/>    |
| [**GetName**](itablet-getname.md)                                     | Recupera una stringa contenente il nome del dispositivo tablet.<br/>               |
| [**GetPlugAndPlayId**](itablet-getplugandplayid.md)                   | Recupera una stringa contenente l'ID Plug and Play per la tavoletta.<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | Recupera i dati di metrica per una proprietà specificata.<br/>                       |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono utilizzare questa interfaccia.

Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITablet** .

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

