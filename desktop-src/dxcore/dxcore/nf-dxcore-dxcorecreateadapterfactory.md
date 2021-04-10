---
title: DXCoreCreateAdapterFactory
description: Crea una factory dell'adattatore DXCore, che è possibile utilizzare per generare altri oggetti DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963336"
---
# <a name="dxcorecreateadapterfactory-function"></a>DXCoreCreateAdapterFactory (funzione)

## <a name="description"></a>Descrizione

Crea una factory dell'adattatore DXCore, che è possibile utilizzare per generare altri oggetti DXCore. Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).

## <a name="parameters"></a>Parametri

### <a name="riid"></a>riid

Tipo: **REFIID**

Riferimento all'identificatore univoco globale (GUID) dell'interfaccia che si desidera venga restituita in *ppvFactory*. Questo dovrebbe essere l'identificatore di interfaccia (IID) di [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **void \* \***

Indirizzo di un puntatore a un'interfaccia con l'IID specificato nel parametro *riid* . In caso di esito positivo, *\* ppvFactory* (l'indirizzo dereferenziato) contiene un puntatore alla Factory di DXCore creata.

## <a name="returns"></a>Restituisce

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se la funzione ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un [codice di errore](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valore restituito|Descrizione|
|-|-|
|E_NOINTERFACE|È stato specificato un valore non valido per *riid*.|
|E_POINTER|`nullptr` fornito per *ppvFactory*.|

## <a name="remarks"></a>Commenti

Per la durata del periodo di tempo in cui è presente un riferimento in un'interfaccia [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , un'interfaccia [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) o un'interfaccia [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , chiamate aggiuntive a **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)o [IDXCoreAdapter:: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) restituiranno puntatori allo stesso oggetto, aumentando il conteggio dei riferimenti dell'interfaccia **IDXCoreAdapterFactory** .

## <a name="see-also"></a>Vedi anche

Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)