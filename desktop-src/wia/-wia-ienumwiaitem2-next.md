---
description: Riempie una matrice di puntatori alle interfacce IWiaItem2.
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'Metodo IEnumWiaItem2:: Next (WIA. h)'
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
ms.openlocfilehash: 2e8800ead0c8f0abaddd0f055f31962d4d55d14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226329"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2:: Next (metodo)

Riempie una matrice di puntatori alle interfacce [**IWiaItem2**](-wia-iwiaitem2.md) .

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

*cElt* \[ in\]
</dt> <dd>

Tipo: **ULONG**

Specifica il numero di elementi di matrice nella matrice indicata dal parametro *ppIWiaItem2* .

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di una matrice di puntatori di interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) . **IEnumWiaItem2:: Next** compila questa matrice con i puntatori di interfaccia.

</dd> <dt>

*pcEltFetched* \[ in uscita\]
</dt> <dd>

Tipo: **ULONG \** _

Nell'output, questo parametro riceve il numero di puntatori di interfaccia effettivamente archiviati nella matrice indicata dal parametro _ppIWiaItem2 *. Quando l'enumerazione è completa, questo parametro contiene zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il sistema di runtime Windows Image Acquisition (WIA) 2,0 rappresenta i dispositivi hardware WIA 2,0 come albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) . Le applicazioni usano il metodo **IEnumWiaItem2:: Next** per ottenere un puntatore a interfaccia **IWiaItem2** per ogni elemento nella cartella corrente dell'albero degli oggetti **IWiaItem2** di un dispositivo hardware.

Per ottenere l'elenco di puntatori, l'applicazione passa una matrice di puntatori dell'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) che alloca. Passa anche il numero di elementi di matrice nel parametro *cElt*. Il metodo **IEnumWiaItem2:: Next** riempie la matrice con i puntatori alle interfacce **IWiaItem2** .

Fino al completamento del processo di enumerazione, il metodo **IEnumWiaItem2:: Next** restituisce S \_ OK. Ogni volta che esegue questa operazione, imposta il valore a cui punta *pcEltFetched* sul numero di elementi inseriti nella matrice. Quando **IEnumWiaItem2:: Next** termina il processo di enumerazione degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) , restituisce \_ false e imposta la posizione di memoria a cui punta *pcEltFetched* su zero.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
