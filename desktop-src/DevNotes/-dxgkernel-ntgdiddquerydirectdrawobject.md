---
description: Esegue una query su una rappresentazione in modalità kernel creata in precedenza di un oggetto DirectDraw Microsoft per le relative funzionalità.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Funzione NtGdiDdQueryDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 557854f70f4f1a55022b16d1bfe045efbc017a13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878118"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>NtGdiDdQueryDirectDrawObject (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Esegue una query su una rappresentazione in modalità kernel creata in precedenza di un oggetto DirectDraw Microsoft per le relative funzionalità.

## <a name="syntax"></a>Sintassi


```C++
BOOL APIENTRY NtGdiDdQueryDirectDrawObject(
  _In_  HANDLE                      hDirectDrawLocal,
  _Out_ DD_HALINFO                  *pHalInfo,
        DWORD                       *pCallBackFlags,
  _Out_ LPD3DNTHAL_CALLBACKS        puD3dCallbacks,
  _Out_ LPD3DNTHAL_GLOBALDRIVERDATA puD3dDriverData,
  _Out_ PDD_D3DBUFCALLBACKS         puD3dBufferCallbacks,
  _Out_ LPDDSURFACEDESC             puD3dTextureFormats,
  _Out_ DWORD                       *puNumHeaps,
  _Out_ VIDEOMEMORY                 *puvmList,
  _Out_ DWORD                       *puNumFourCC,
  _Out_ DWORD                       *puFourCC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDrawLocal* \[ in\]
</dt> <dd>

Handle per il dispositivo DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*pHalInfo* \[ out\]
</dt> <dd>

Puntatore a una [**struttura \_ HALINFO DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) che verrà compilata con le funzionalità del dispositivo. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Puntatore a un buffer fornito dal chiamante che archivia i flag di callback segnalati dal driver. Il buffer deve essere di dimensioni 3 \* sizeof (DWORD) e archivia i flag di callback nell'ordine seguente: pCallBackFlags \[ 0 \] per i flag nei [**\_ callback GG**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks), PCallBackFlags \[ 1 per i \] flag in [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)e pCallBackFlags \[ 2 per i \] flag in [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puD3dCallbacks* \[ out\]
</dt> <dd>

Puntatore a una tabella di puntatori di callback Direct3D. La tabella viene compilata con i puntatori alle funzioni all'interno Gdi32.dll che imitano un driver di visualizzazione Direct3D. Questa tabella di callback è identica alla \_ struttura D3DHAL D3DCALLBACKS descritta nella documentazione di DDK.

</dd> <dt>

*puD3dDriverData* \[ out\]
</dt> <dd>

Puntatore ai [**dati \_ GLOBALDRIVERDATA di D3DHAL**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) , come descritto nella documentazione di DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ out\]
</dt> <dd>

Puntatore a una tabella di puntatori di callback. La tabella viene compilata con i puntatori alle funzioni all'interno Gdi32.dll che imitano un driver di visualizzazione Direct3D. Questa tabella di callback è identica alla \_ struttura DDEXEBUFCALLBACKS di DDHAL, che esegue il mapping alla struttura [**DD \_ D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) descritta nella documentazione di DDK, con la differenza che i membri XxxD3DBuffer in **DD \_ D3DBUFCALLBACKS** vengono sostituiti con XxxExecuteBuffer in DDHAL \_ DDEXEBUFCALLBACKS.

</dd> <dt>

*puD3dTextureFormats* \[ out\]
</dt> <dd>

Puntatore a una matrice di strutture [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che definiscono il set di formati di trama consentiti.

</dd> <dt>

*puNumHeaps* \[ out\]
</dt> <dd>

Puntatore al membro **dwNumHeaps** di [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**. Il membro **dwNumHeaps** specifica il numero di heap di memoria in *puvmList*. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puvmList* \[ out\]
</dt> <dd>

Puntatore a un elenco di descrittori di heap di memoria video. Può essere **null**. Questo parametro non viene utilizzato perché la gestione della memoria video viene gestita interamente in modalità kernel.

</dd> <dt>

*puNumFourCC* \[ out\]
</dt> <dd>

Puntatore al membro **puNumFourCCCodes** di [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. Il membro **puNumFourCCCodes** specifica il numero di codici di [quattro caratteri (fourcc)](../directshow/fourcc-codes.md) supportati dal driver. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puFourCC* \[ out\]
</dt> <dd>

Puntatore a un elenco di formati di superficie supportati per i [codici a quattro caratteri (fourcc)](../directshow/fourcc-codes.md) . Può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'esito è positivo, la funzione restituisce **true**. in caso contrario, restituisce **false**.

## <a name="remarks"></a>Commenti

Una chiamata a questa funzione è progettata per essere eseguita in un processo in due passaggi. Nel primo passaggio, *puFourCC*, *puvmList* e *PuD3dTextureFormats* devono essere **null** e [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) compilerà [**gg \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **gg \_ HALINFO**.**vmiData**. **dwNumHeaps** e [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** con il numero di voci da restituire. Nella seconda chiamata, il chiamante deve allocare matrici della dimensione indicata e passare tali puntatori invece dei valori **null** nei parametri *puFourCC*, *puvmList* e *puD3dTextureFormats* . Le matrici verranno quindi popolate con i dati appropriati.

Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) . Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
