---
description: Riempie una matrice di puntatori alle interfacce IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: Metodo IEnumWiaItem2::Next (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cf884375f504bb801bcebcaad3f75b23c5f82956ce3a1d45dd5a50bfa5f8e53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451141"
---
# <a name="ienumwiaitem2next-method"></a>Metodo IEnumWiaItem2::Next

Riempie una matrice di puntatori [**alle interfacce IWiaItem2.**](-wia-iwiaitem2.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cElt* \[ Pollici\]
</dt> <dd>

Tipo: **ULONG**

Specifica il numero di elementi della matrice indicati dal *parametro ppIWiaItem2.*

</dd> <dt>

*ppIWiaItem2* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di una matrice di puntatori a interfaccia [**IWiaItem2.**](-wia-iwiaitem2.md) **IEnumWiaItem2::Next** riempie questa matrice con puntatori a interfaccia.

</dd> <dt>

*pcEltFetched* \[ in, out\]
</dt> <dd>

Tipo: **ULONG \***

Nell'output questo parametro riceve il numero di puntatori a interfaccia effettivamente archiviati nella matrice indicata dal *parametro ppIWiaItem2.* Al termine dell'enumerazione, questo parametro contiene zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il sistema di run-time Windows Image Acquisition (WIA) 2.0 rappresenta i dispositivi hardware WIA 2.0 come albero gerarchico di oggetti [**IWiaItem2.**](-wia-iwiaitem2.md) Le applicazioni usano **il metodo IEnumWiaItem2::Next** per ottenere un puntatore di interfaccia **IWiaItem2** per ogni elemento nella cartella corrente dell'albero di oggetti **IWiaItem2** di un dispositivo hardware.

Per ottenere l'elenco dei puntatori, l'applicazione passa una matrice di puntatori a interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) che alloca. Passa anche il numero di elementi della matrice nel parametro *cElt*. Il **metodo IEnumWiaItem2::Next** riempie la matrice con puntatori **alle interfacce IWiaItem2.**

Fino al completamento del processo di enumerazione, il **metodo IEnumWiaItem2::Next** restituisce S \_ OK. Ogni volta che lo fa, imposta il valore a cui punta *pcEltFetched* sul numero di elementi inseriti nella matrice. Quando **IEnumWiaItem2::Next** completa il processo di enumerazione degli oggetti [**IWiaItem2,**](-wia-iwiaitem2.md) restituisce S FALSE e imposta la posizione di memoria a cui punta \_ *pcEltFetched* su zero.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppIWiaItem2.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
