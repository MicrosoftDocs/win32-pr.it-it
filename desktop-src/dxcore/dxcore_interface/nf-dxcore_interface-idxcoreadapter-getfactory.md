---
title: IDXCoreAdapter::GetFactory
description: "Recupera un puntatore di interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) all'oggetto factory dell'adattatore dxcore. | IDXCoreAdapter:: GetFactory"
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234776"
---
# <a name="idxcoreadaptergetfactory-method"></a>Metodo IDXCoreAdapter:: GetFactory

Recupera un puntatore di interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) all'oggetto factory dell'adattatore dxcore. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintassi

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Parametri

### <a name="riid"></a>riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvFactory*. Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **void \* \***

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* . In caso di esito positivo, *\* ppvFactory* (l'indirizzo dereferenziato) contiene un puntatore all'oggetto factory dell'adapter DXCore esistente. Prima di restituire, la funzione incrementa il conteggio dei riferimenti nell'interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) dell'oggetto Factory.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` fornito per *ppvFactory*.|

## <a name="remarks"></a>Commenti

Per la durata del periodo di tempo in cui è presente un riferimento in un'interfaccia [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , un'interfaccia [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) o un'interfaccia [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , chiamate aggiuntive a [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList:: GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory]() restituiranno puntatori allo stesso oggetto, aumentando il conteggio dei riferimenti dell'interfaccia **IDXCoreAdapterFactory** .

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
