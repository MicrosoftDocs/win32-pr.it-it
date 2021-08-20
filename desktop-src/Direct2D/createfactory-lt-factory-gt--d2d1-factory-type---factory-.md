---
title: Funzione D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) (D2d1.h)
description: Crea un oggetto factory che può essere usato per creare risorse Direct2D. | Funzione D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) (D2d1.h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Funzione Direct2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory )
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af5635a6f996ea6cd3af2c3b3022efa054cd27605430c8230143980e00b9abbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826470"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a>Funzione D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,Factory) \* \*

Crea un oggetto factory che può essere usato per creare risorse Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Parametri di template



| Parametro | Descrizione                                                 |
|-----------|-------------------------------------------------------------|
| *Fabbrica* | Tipo di [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) da creare. |



 

## <a name="parameters"></a>Parametri



| Parametro     | Descrizione                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | Modello di threading della factory e delle risorse create.                |
| *factory*     | Quando questo metodo viene restituito, contiene l'indirizzo di un puntatore alla nuova factory. |



 

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="examples"></a>Esempio

Nell'esempio seguente viene creata una factory.


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7, Windows Vista con SP2 e Aggiornamento piattaforma per Windows app desktop di Vista \[ \| app UWP\]<br/>                          |
| Server minimo supportato<br/> | Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per Windows app desktop di Windows Server 2008 \[ app desktop \| UWP\]<br/> |
| Telefono minimo supportato<br/>  | Windows Phone 8.1 \[ Windows Phone silverlight 8.1 e Windows Runtime\]<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Libreria<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

