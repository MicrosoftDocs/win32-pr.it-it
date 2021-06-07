---
UID: NF:directml.DMLCreateDevice1
title: Funzione DMLCreateDevice1
description: Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12.
helpviewer_keywords:
- DMLCreateDevice1
- DMLCreateDevice1 function
- direct3d12.dmlcreatedevice1
- directml/DMLCreateDevice1
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DMLCreateDevice1
- directml/DMLCreateDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- DirectML.dll
api_name:
- DMLCreateDevice1
ms.openlocfilehash: f722b12208bd808f01e177feb907f94c33541496
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417449"
---
# <a name="dmlcreatedevice1-function-directmlh"></a>Funzione DMLCreateDevice1 (directml.h)

Crea un dispositivo DirectML per un determinato dispositivo Direct3D 12.

> [!IMPORTANT]
> Questa API è disponibile come parte del pacchetto ridistribuibile autonomo DirectML (vedere [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versione 1.4 e successive). Vedere anche [Cronologia delle versioni di DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintassi

```cpp
HRESULT DMLCreateDevice1(
  ID3D12Device            *d3d12Device,
  DML_CREATE_DEVICE_FLAGS flags,
  DML_FEATURE_LEVEL       minimumFeatureLevel,
  REFIID                  riid,
  void                    **ppv
);
```

## <a name="parameters"></a>Parametri

`d3d12Device`

Tipo: <b> <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>*</b>

Puntatore a un [dispositivo ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) che rappresenta il dispositivo Direct3D 12 su cui creare il dispositivo DirectML. DirectML supporta qualsiasi livello di funzionalità D3D e i dispositivi Direct3D 12 creati in qualsiasi scheda, incluso WARP. Tuttavia, non tutte le funzionalità di DirectML possono essere disponibili a seconda delle funzionalità del dispositivo Direct3D 12. Per [altre informazioni, vedere IDMLDevice::CheckFeatureSupport.](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)

Se la chiamata a **DMLCreateDevice1** ha esito positivo, il dispositivo DirectML mantiene un riferimento sicuro al dispositivo Direct3D 12 fornito.

`flags`

Tipo: <b>DML_CREATE_DEVICE_FLAGS</b>

Valore [DML_CREATE_DEVICE_FLAGS](/windows/win32/api/directml/ne-directml-dml_create_device_flags) che specifica opzioni di creazione del dispositivo aggiuntive.

`minimumFeatureLevel`

Tipo: <b>DML_FEATURE_LEVEL</b>

Valore [DML_FEATURE_LEVEL](/windows/win32/api/directml/ne-directml-dml_feature_level) che specifica il supporto minimo del livello di funzionalità richiesto.

Questo parametro può essere utile per i chiamanti che richiedono una versione specifica di DirectML, ma che possono trovarsi a chiamare in una versione precedente di DirectML. Ciò può verificarsi, ad esempio, quando l'utente esegue l'applicazione in una versione precedente di Windows 10.

Le applicazioni che dipendono in modo esplicito dalle funzionalità introdotte in un determinato livello di funzionalità possono specificarlo come *minimumFeatureLevel*. In questo modo si garantisce che **DMLCreateDevice1** non riuscirà a meno che l'implementazione sottostante non sia almeno in grado di questo livello di funzionalità minimo richiesto. 

Si noti che poiché questo parametro specifica un *livello* di funzionalità minimo, il dispositivo DirectML sottostante può infatti supportare un livello di funzionalità superiore al livello minimo richiesto. Al termine della creazione del dispositivo, è possibile eseguire una query su tutti i livelli di funzionalità supportati da questo dispositivo usando [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

`riid`

Tipo: <b>REFIID</b>

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera restituire nel <i>dispositivo</i>. Si prevede che sia il GUID di [IDMLDevice.](/windows/win32/api/directml/nn-directml-idmldevice)

`ppv`

Tipo: \_ COM \_ Outptr opt \_ \_ <b>void**</b>

Puntatore a un blocco di memoria che riceve un puntatore al dispositivo. Si tratta dell'indirizzo di un puntatore a [un oggetto IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)che rappresenta il dispositivo DirectML creato.


## <a name="return-value"></a>Valore restituito

Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Se la funzione ha esito positivo, restituisce <b>S_OK</b>. In caso contrario, restituisce un [codice di errore HRESULT.](/windows/desktop/winprog/windows-data-types)

Se questa versione di DirectML non supporta *il valore minimumFeatureLevel* richiesto, questa funzione restituirà DXGI_ERROR_UNSUPPORTED **.**

Per usare i livelli di debug DirectML, è necessario installare la funzionalità degli strumenti di grafica su richiesta. Se il [flag DML_CREATE_DEVICE_FLAG_DEBUG](/windows/win32/api/directml/ne-directml-dml_create_device_flags) viene specificato nei *flag* e i livelli di debug non sono installati, **DMLCreateDevice1** restituisce **DXGI_ERROR_SDK_COMPONENT_MISSING**.

## <a name="remarks"></a>Commenti

È stata introdotta una versione più recente di questa funzione, [DMLCreateDevice1,]()in DirectML versione 1.1.0. **DMLCreateDevice1** equivale a chiamare **DMLCreateDevice1** e a fornire *un valore minimumFeatureLevel* [DML_FEATURE_LEVEL_1_0](/windows/win32/api/directml/ne-directml-dml_feature_level).

## <a name="availability"></a>Disponibilità

Questa API è stata introdotta in DirectML versione `1.1.0` .

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Piattaforma di destinazione** | Windows |
| **Intestazione** | directml.h |
| **Libreria** | DirectML.lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Vedi anche

* [DML_FEATURE_LEVEL enumerazione](/windows/win32/api/directml/ne-directml-dml_feature_level)
* [Cronologia delle versioni di DirectML](../dml-version-history.md)
* [Cronologia a livello di funzionalità DirectML](/windows/win32/direct3d12/dml-feature_level-history)    
* [Uso del livello di debug DirectML](../dml-debug-layer.md)