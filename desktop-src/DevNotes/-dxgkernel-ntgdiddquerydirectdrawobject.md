---
description: Esegue una query su una rappresentazione in modalità kernel creata in precedenza di un oggetto Microsoft DirectDraw per le relative funzionalità.
ms.assetid: ec07c7ef-4c57-4ed9-849b-f30692cc3181
title: Funzione NtGdiDdQueryDirectDrawObject (Ntgdi.h)
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
ms.openlocfilehash: 2cd87bc1cc278f8ee680dbd458ed3b92cc699a060021a91535de66996376db84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103821"
---
# <a name="ntgdiddquerydirectdrawobject-function"></a>Funzione NtGdiDdQueryDirectDrawObject

\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo. Usare invece DirectDraw e Microsoft Direct3DAPIs. queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]

Esegue una query su una rappresentazione in modalità kernel creata in precedenza di un oggetto Microsoft DirectDraw per le relative funzionalità.

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

*hDirectDrawLocal* \[ Pollici\]
</dt> <dd>

Handle per il dispositivo DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*pHalInfo* \[ Cambio\]
</dt> <dd>

Puntatore a [**una struttura \_ DD HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo) che verrà riempita con le funzionalità del dispositivo. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*pCallBackFlags* 
</dt> <dd>

Puntatore a un buffer fornito dal chiamante che archivia i flag di callback segnalati dal driver. Il buffer deve avere dimensioni 3 sizeof(DWORD) e archivia i flag di callback nell'ordine \* seguente: pCallBackFlags 0 per i flag \[ \] in [**DD \_ CALLBACKS,**](/windows/win32/api/ddrawint/ns-ddrawint-dd_callbacks)pCallBackFlags 1 per i \[ flag in \] [**DD \_ SURFACECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surfacecallbacks)e pCallBackFlags 2 per i flag \[ in \] [**DD \_ PALETTECALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_palettecallbacks). Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puD3dCallbacks* \[ Cambio\]
</dt> <dd>

Puntatore a una tabella di puntatori di callback Direct3D. La tabella viene riempita con puntatori a funzioni all'interno Gdi32.dll che imitano un driver di visualizzazione Direct3D. Questa tabella di callback è identica alla struttura \_ D3DHAL D3DCALLBACKS illustrata nella documentazione di DDK.

</dd> <dt>

*puD3dDriverData* \[ Cambio\]
</dt> <dd>

Puntatore [**ai dati D3DHAL \_ GLOBALDRIVERDATA,**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata) come descritto nella documentazione di DDK.

</dd> <dt>

*puD3dBufferCallbacks* \[ Cambio\]
</dt> <dd>

Puntatore a una tabella di puntatori di callback. La tabella viene riempita con puntatori a funzioni all'interno Gdi32.dll che imitano un driver di visualizzazione Direct3D. Questa tabella di callback è identica alla struttura DDHAL DDEXEBUFCALLBACKS, che esegue il mapping alla struttura \_ [**\_ DD D3DBUFCALLBACKS**](/windows/win32/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks) descritta nella documentazione di DDK, ad eccezione del fatto che i membri XxxD3DBuffer in **\_ DD D3DBUFCALLBACKS** vengono sostituiti con XxxExecuteBuffer in \_ DDHAL DDEXEBUFCALLBACKS.

</dd> <dt>

*puD3dTextureFormats* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice [**di strutture DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che definiscono il set di formati di trama consentiti.

</dd> <dt>

*puNumHeaps* \[ Cambio\]
</dt> <dd>

Puntatore al **membro dwNumHeaps** [**di DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**vmiData**. Il **membro dwNumHeaps** specifica il numero di heap di memoria in *puvmList*. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puvmList* \[ Cambio\]
</dt> <dd>

Puntatore a un elenco di descrittori dell'heap della memoria video. Può essere **NULL.** Questo parametro non viene usato perché la gestione della memoria video viene gestita interamente in modalità kernel.

</dd> <dt>

*puNumFourCC* \[ Cambio\]
</dt> <dd>

Puntatore al **membro puNumFourCCCodes** [**di DD \_ HALINFO.**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo)**ddCaps**. Il **membro puNumFourCCCodes** specifica il numero di codici [four-character codes (FOURCC)](../directshow/fourcc-codes.md) supportati dal driver. Per informazioni dettagliate, vedere la documentazione di DDK.

</dd> <dt>

*puFourCC* \[ Cambio\]
</dt> <dd>

Puntatore a un elenco di [formati di superficie four-character codes (FOURCC)](../directshow/fourcc-codes.md) supportati. Può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, questa funzione restituisce **TRUE;** in caso contrario restituisce **FALSE.**

## <a name="remarks"></a>Commenti

Una chiamata a questa funzione è progettata per essere effettuata in un processo in due passaggi. Nel primo passaggio *puFourCC,* *puvmList* e *puD3dTextureFormats* devono essere **NULL** e [**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject) riempirà [**DD \_ HALINFO**](/windows/win32/api/ddrawint/ns-ddrawint-dd_halinfo).**ddCaps**. **dwNumFourCCCodes**, **DD \_ HALINFO**.**vmiData**. **dwNumHeaps** e [**D3DHAL \_ GLOBALDRIVERDATA**](/windows-hardware/drivers/ddi/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata).**dwNumTextureFormats** con il numero di voci da restituire. Nella seconda chiamata, il chiamante deve allocare matrici delle dimensioni indicate e passare tali puntatori anziché **valori NULL** nei parametri *puFourCC*, *puvmList* e *puD3dTextureFormats.* Le matrici verranno quindi popolate con i dati appropriati.

Si consiglia alle applicazioni di usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) per creare e gestire oggetti dispositivo grafico. Questi costrutti astrarre il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di basso livello per grafica](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdQueryDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddquerydirectdrawobject)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> </dl>

 

 
