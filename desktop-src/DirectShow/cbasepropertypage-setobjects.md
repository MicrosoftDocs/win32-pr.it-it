---
description: Il metodo SetObjects fornisce puntatori IUnknown per gli oggetti associati alla pagina delle proprietà. Questo metodo implementa il metodo IPropertyPage::SetObjects.
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Metodo CBasePropertyPage.SetObjects (Cprop.h)
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
ms.openlocfilehash: 9e5c29d1ddc646ef05faad2bc283887265e8b85109fcb679924d9a5641ef13fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823026"
---
# <a name="cbasepropertypagesetobjects-method"></a>Metodo CBasePropertyPage.SetObjects

Il `SetObjects` metodo fornisce **puntatori IUnknown** per gli oggetti associati alla pagina delle proprietà. Questo metodo implementa il **metodo IPropertyPage::SetObjects.**

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

Specifica il numero di **puntatori IUnknown** nella matrice specificata da *ppUnk*.

</dd> <dt>

*ppUnk* 
</dt> <dd>

Specifica una matrice di **puntatori IUnknown.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                  | Descrizione                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione completata.<br/>                   |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | Argomento del puntatore **NULL.**<br/> |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Errore imprevisto.<br/>        |



 

## <a name="remarks"></a>Commenti

Anche *se ppUnk* specifica una matrice di **puntatori IUnknown,** la **classe CBasePropertyPage** è progettata solo per supportare un oggetto associato. Se *cObjects* è maggiore di 1, il metodo restituisce E \_ UNEXPECTED.

Se *cObjects* è uguale a 1, questo metodo chiama il metodo [**CBasePropertyPage::OnConnect.**](cbasepropertypage-onconnect.md) Se *cObjects è* uguale a 0, questo metodo chiama il metodo [**CBasePropertyPage::OnDisconnect.**](cbasepropertypage-ondisconnect.md) La classe derivata deve eseguire l'override di entrambi questi metodi. Per informazioni dettagliate, vedere le osservazioni relative a tali metodi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (include Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




