---
description: Rappresenta il contesto della tavoletta.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interfaccia ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319166"
---
# <a name="itabletcontextp-interface"></a>Interfaccia ITabletContextP

Rappresenta il contesto della tavoletta.

## <a name="members"></a>Membri

L'interfaccia **ITabletContextP** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletContextP** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITabletContextP** dispone di questi metodi.



| Metodo                                                                                           | Descrizione                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**IsTopMostHook**](itabletcontextp-istopmosthook.md)                                           | Indica se il contesto del tablet è nell'hook superiore.<br/>             |
| [**Overlap**](itabletcontextp-overlap.md)                                                       | Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.<br/>      |
| [**TrackInputRect**](itabletcontextp-trackinputrect.md)                                         | Aggiorna il digitalizzatore del Tablet alle coordinate del mapping della posizione della finestra.<br/> |
| [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | Consente di accedere alla memoria condivisa tra i thread del tablet.<br/>             |
| [**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)           | Consente di accedere alla memoria condivisa tra i thread del tablet.<br/>             |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono utilizzare questa interfaccia.

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) è disponibile solo in Windows Vista e versioni successive.

Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITabletContextP** .

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

