---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Crea un oggetto factory usato per la creazione successiva di singoli oggetti DWriteCore.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 43e43e00385e10f0da0ba459cdc16e84562b72ec
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955024"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>Funzione DWriteCoreCreateFactory (dwrite_core.h)

Crea un oggetto factory usato per la creazione successiva di singoli oggetti DWriteCore.

> [!IMPORTANT]
> Questa API è disponibile come parte dell'implementazione DWriteCore di [DirectWrite.](../direct-write-portal.md) DWriteCore è un'implementazione di DirectWrite, eseguibile su Windows fino alla versione 8, che offre opportunità per l'uso su più piattaforme. Per altre informazioni ed esempi di codice, vedi [Panoramica di DWriteCore.](/windows/win32/directwrite/dwritecore-overview)

## <a name="syntax"></a>Sintassi
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>Parametri

`factoryType`

Tipo: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

Valore che specifica se l'oggetto factory verrà condiviso, isolato o limitato.

`iid`

Tipo: <b>REFIID</b>

Valore GUID che identifica l'interfaccia della factory DirectWrite, ad esempio __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).

`factory`

Tipo: <b>IUnknown**</b>

Indirizzo di un puntatore all'oggetto factory DirectWrite appena creato.

## <a name="return-value"></a>Valore restituito

Tipo: <b>HRESULT</b>

Se questo metodo ha esito positivo, restituisce <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. In caso contrario, restituisce un <b xmlns:loc="http://microsoft.com/wdcml/l10n">codice di errore HRESULT.</b>

## <a name="examples"></a>Esempio

Vedere [l'argomento di panoramica DWriteCore](/windows/win32/directwrite/dwritecore-overview) e l'app di esempio [DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Commenti

Dal punto di vista funzionale è uguale alla [funzione DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) esportata dalla versione di sistema di DirectWrite. La funzione DWriteCore ha un nome diverso per evitare ambiguità.

## <a name="requirements"></a>Requisiti
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimo supportato** | Windows 10, Project Dispositivi [app Win32] |
| **Intestazione** | dwrite.h (includere dwrite_core.h) |
