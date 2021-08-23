---
description: Imposta un nuovo callback dell'applicazione per il filtro di elaborazione delle immagini da utilizzare per l'inoltro delle chiamate.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: Metodo IWiaImageFilter::SetNewCallback (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.SetNewCallback
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: abb279faba1c5174fc39ebdfe30a4a8cde8cabf86e8b86599f8d3ab9cc3247cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450491"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>Metodo IWiaImageFilter::SetNewCallback

Imposta un nuovo callback dell'applicazione per il filtro di elaborazione delle immagini da utilizzare per l'inoltro delle chiamate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaTransferCallback* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Specifica un puntatore all'interfaccia [**IWiaTransferCallback dell'applicazione.**](-wia-iwiatransfercallback.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Non chiamare questo metodo direttamente dall'applicazione.

Il filtro di elaborazione delle immagini è necessario per rilasciare l'interfaccia di callback dell'applicazione archiviata in precedenza prima di impostare il nuovo callback.

Se *pWiaTransferCallback* è **NULL,** il filtro di elaborazione delle immagini deve semplicemente rilasciare il callback dell'applicazione precedente e restituire S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




