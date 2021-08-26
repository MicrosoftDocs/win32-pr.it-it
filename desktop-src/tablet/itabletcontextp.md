---
description: Rappresenta il contesto del tablet.
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
ms.openlocfilehash: da5c26a0a9d7d080a9787fef0b7ba2fdb919e473fd66c989fca478c4ac7d0ac3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883521"
---
# <a name="itabletcontextp-interface"></a>Interfaccia ITabletContextP

Rappresenta il contesto del tablet.

## <a name="members"></a>Membri

**L'interfaccia ITabletContextP** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletContextP** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITabletContextP** include questi metodi.



| Metodo                                                                                           | Descrizione                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**IsTopMostHook**](itabletcontextp-istopmosthook.md)                                           | Indica se il contesto del tablet è in primo piano.<br/>             |
| [**Overlap**](itabletcontextp-overlap.md)                                                       | Sposta un contesto del tablet nella parte anteriore o posteriore della coda di input.<br/>      |
| [**TrackInputRect**](itabletcontextp-trackinputrect.md)                                         | Aggiorna il digitalizzatore tablet alle coordinate di mapping della posizione della finestra.<br/> |
| [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | Fornisce l'accesso alla memoria condivisa tra i thread del tablet.<br/>             |
| [**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)           | Fornisce l'accesso alla memoria condivisa tra i thread del tablet.<br/>             |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono usare questa interfaccia.

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) è disponibile solo in Windows Vista e versioni successive.

Il codice seguente descrive come viene definita **l'interfaccia ITabletContextP.**

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
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

