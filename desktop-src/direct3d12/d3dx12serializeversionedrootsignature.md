---
title: Funzione D3DX12SerializeVersionedRootSignature (D3dx12.h)
description: Consente di abilitare le funzionalità della firma radice 1.1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la compilazione delle firme radice. Questo metodo helper ricostruisce una firma radice della versione 1.0 quando la versione 1.1 non è supportata.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- Funzione D3DX12SerializeVersionedRootSignature
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f69e3bf66bcbad61e3d9bf676038f27511f756d7a3a473be2c513553862eb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851155"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>Funzione D3DX12SerializeVersionedRootSignature

Consente di abilitare le funzionalità della firma radice 1.1 quando sono disponibili e non richiede la gestione di due percorsi di codice per la compilazione delle firme radice. Questo metodo helper ricostruisce una firma radice della versione 1.0 quando la versione 1.1 non è supportata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRootSignatureDesc* \[ Pollici\]
</dt> <dd>

Tipo: **const D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC \***

Specifica un [**D3D12 \_ VERSIONED \_ ROOT SIGNATURE \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) che contiene una descrizione di qualsiasi versione di una firma radice.

</dd> <dt>

*MaxVersion* 
</dt> <dd>

Tipo: **D3D \_ ROOT SIGNATURE \_ \_ VERSION**

Specifica il numero massimo supportato [**di D3D \_ ROOT SIGNATURE \_ \_ VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).

</dd> <dt>

*ppBlob* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* ID3DBlob**

Puntatore a un blocco di memoria che riceve un puntatore [**all'interfaccia ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere alla firma radice serializzata.

</dd> <dt>

*ppErrorBlob* \[ out, facoltativo\]
</dt> <dd>

Tipo: **\* \* ID3DBlob**

Puntatore a un blocco di memoria che riceve un puntatore [**all'interfaccia ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) che è possibile usare per accedere ai messaggi di errore del serializzatore oppure **NULL** se non sono presenti errori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce **S \_ OK in** caso di esito positivo. In caso contrario, restituisce uno dei codici restituiti [Direct3D 12.](d3d12-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questa funzione è stata rilasciata in Windows 10'aggiornamento dell'anniversario (14393). Per supportare le Windows 10 precedenti, l'uso di questa funzione richiede che d3d12.lib sia configurato per il *caricamento ritardato.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

