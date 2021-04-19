---
title: Metodo GetNext IWMDRMLicense (wmdrmsdk. h)
description: Il metodo GetNext carica le informazioni relative all'elemento successivo nell'elenco.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Formato Windows Media metodo GetNext
- Metodo GetNext, formato Windows Media, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetNext
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326293"
---
# <a name="iwmdrmlicensegetnext-method"></a>Metodo IWMDRMLicense:: GetNext

Il metodo **GetNext** carica le informazioni relative all'elemento successivo nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt> </dl> | È necessario un elenco di revoche di contenuti aggiornato.<br/> |
| <dl> <dt>**ERRORE \_ nessun \_ altro \_ elemento**</dt> </dl>      | Non sono presenti altri elementi nell'elenco.<br/>          |
| <dl> <dt>**\_OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

I metodi dell'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) forniscono dati relativi a una singola licenza alla volta. L'oggetto sottostante contiene un elenco di una o più licenze. Quando si chiama questo metodo, l'interfaccia sposta i relativi riferimenti interni alla licenza successiva nell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





