---
title: Metodo GetNext IWMDRMLicense (Wmdrmsdk.h)
description: Il metodo GetNext carica le informazioni sull'elemento successivo nell'elenco.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- Metodo GetNext windows Media Format
- Metodo GetNext windows Media Format , interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense windows Media Format , metodo GetNext
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
ms.openlocfilehash: dc0905bc695d1317cc7e4a6a1933292ad68afa8f3e3aadb9572e7a7185f4089c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847138"
---
# <a name="iwmdrmlicensegetnext-method"></a>Metodo IWMDRMLicense::GetNext

Il **metodo GetNext** carica le informazioni sull'elemento successivo nell'elenco.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNext();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM RIV TROPPO \_ \_ \_ PICCOLO**</dt> </dl> | È necessario un elenco di revoche di contenuto aggiornato.<br/> |
| <dl> <dt>**ERRORE \_ NESSUN \_ ALTRO \_ ELEMENTO**</dt> </dl>      | Non sono presenti altri elementi nell'elenco.<br/>          |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Il metodo è riuscito.<br/>                         |



 

## <a name="remarks"></a>Commenti

I metodi [**dell'interfaccia IWMDRMLicense**](iwmdrmlicense.md) forniscono dati su una singola licenza alla volta. L'oggetto sottostante contiene un elenco di una o più licenze. Quando si chiama questo metodo, l'interfaccia sposta i riferimenti interni alla licenza successiva nell'elenco.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





