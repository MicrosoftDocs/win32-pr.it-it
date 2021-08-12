---
description: Inizializza il filtro. Chiamato da Windows Image Acquisition (WIA) 2.0 prima del download di ogni immagine.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: Metodo IWiaImageFilter::InitializeFilter (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 43b818c3adc9926c4ba27f11f5d489ffc0b97e4443d0427e7a12067e9062072a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440446"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>Metodo IWiaImageFilter::InitializeFilter

Inizializza il filtro. Chiamato da Windows Image Acquisition (WIA) 2.0 prima del download di ogni immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaItem2* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Specifica un puntatore [**all'elemento IWiaItem2**](-wia-iwiaitem2.md) che rappresenta l'immagine di anteprima.

</dd> <dt>

*pWiaTransferCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Specifica un puntatore all'interfaccia [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando un'applicazione chiama [**Download**](-wia-iwiatransfer-download.md) e quando un'applicazione chiama la funzione del componente di anteprima di WIA 2.0. `GetNewPreview` **IWiaImageFilter::InitializeFilter** archivia i riferimenti a *pWiaItem2* e *pWiaTransferCallback* da passare a queste funzioni. Questi due puntatori a interfaccia devono essere archiviati come variabili membro e [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve essere chiamato per ognuno. I puntatori a interfaccia sono necessari anche nell'implementazione del filtro di [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) e [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante l'acquisizione dell'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
