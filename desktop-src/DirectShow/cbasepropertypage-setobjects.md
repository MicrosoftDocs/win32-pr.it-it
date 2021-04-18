---
description: 'Il metodo seobjects fornisce i puntatori IUnknown per gli oggetti associati alla pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: seobjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Metodo CBasePropertyPage. seobjects (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330411"
---
# <a name="cbasepropertypagesetobjects-method"></a>Metodo CBasePropertyPage. seobjects

Il `SetObjects` metodo fornisce i puntatori **IUnknown** per gli oggetti associati alla pagina delle proprietà. Questo metodo implementa il metodo **IPropertyPage:: Seobjects** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cObjects* 
</dt> <dd>

Specifica il numero di puntatori **IUnknown** nella matrice specificata da *ppunk*.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Specifica una matrice di puntatori **IUnknown** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Esito positivo.<br/>                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Argomento puntatore **null** .<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Errore imprevisto.<br/>        |



 

## <a name="remarks"></a>Commenti

Sebbene *ppunk* specifichi una matrice di puntatori **IUnknown** , la classe **CBasePropertyPage** è progettata solo per supportare un oggetto associato. Se *CObjects* è maggiore di 1, il metodo restituisce E \_ imprevisto.

Se *CObjects* è uguale a 1, questo metodo chiama il metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) . Se *CObjects* è uguale a 0, questo metodo chiama il metodo [**CBasePropertyPage:: Disconnect**](cbasepropertypage-ondisconnect.md) . La classe derivata deve eseguire l'override di entrambi i metodi; per informazioni dettagliate, vedere la sezione Osservazioni per tali metodi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




