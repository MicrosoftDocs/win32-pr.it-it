---
description: 'Costruttore CMediaControl.CMediaControl : metodo costruttore.'
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Costruttore CMediaControl.CMediaControl (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099209"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>Costruttore CMediaControl.CMediaControl

Metodo del costruttore.

## <a name="syntax"></a>Sintassi


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Puntatore al nome dell'oggetto a scopo di debug.

</dd> <dt>

*Punk* 
</dt> <dd>

Puntatore al proprietario di questo oggetto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Allocare il *parametro pName* nella memoria statica. Questo nome viene visualizzato nel terminale di debug al momento della creazione e dell'eliminazione dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaControl**](cmediacontrol.md)
</dt> </dl>

 

 




