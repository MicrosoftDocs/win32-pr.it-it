---
title: DXCoreCreateAdapterFactory
description: Crea una factory di adattatori DXCore, che è possibile usare per generare altri oggetti DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 90567d732f6febc5d95b460b2ff88929dd12b2f22275de9db0d6bc5f88ef99ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985181"
---
# <a name="dxcorecreateadapterfactory-function"></a>Funzione DXCoreCreateAdapterFactory

## <a name="description"></a>Descrizione

Crea una factory di adattatori DXCore, che è possibile usare per generare altri oggetti DXCore. Per indicazioni sulla programmazione ed esempi di codice, vedere [Uso di DXCore per enumerare gli adattatori.](../dxcore-enum-adapters.md)

## <a name="parameters"></a>Parametri

### <a name="riid"></a>Riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si vuole restituire in *ppvFactory.* Si prevede che sia l'identificatore di interfaccia (IID) di [IDXCoreAdapterFactory.](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **\* \* void**

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel *parametro riid.* Al completamento della restituzione, *\* ppvFactory* (l'indirizzo dereferenziato) contiene un puntatore alla factory DXCore creata.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [**codice di errore HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valore restituito|Descrizione|
|-|-|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` è stato fornito per *ppvFactory*.|

## <a name="remarks"></a>Commenti

Per la durata dell'esistenza di un riferimento in [un'interfaccia IDXCoreAdapterFactory,](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) [un'interfaccia IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) o un'interfaccia [IDXCoreAdapter,](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) le chiamate aggiuntive a **DXCoreCreateAdapterFactory,** [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) restituiranno puntatori allo stesso oggetto, aumentando il conteggio dei riferimenti dell'interfaccia **IDXCoreAdapterFactory.**

## <a name="see-also"></a>Vedi anche

[Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)