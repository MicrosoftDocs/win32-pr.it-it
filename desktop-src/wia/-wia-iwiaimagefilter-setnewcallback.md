---
description: Imposta un nuovo callback dell'applicazione per il filtro di elaborazione dell'immagine da utilizzare per l'invio delle chiamate.
ms.assetid: 25b86f1d-96c8-4150-9147-13be9b1dd50c
title: 'Metodo IWiaImageFilter:: SetNewCallback (WIA. h)'
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
ms.openlocfilehash: 16325d854f7b17c62e6fb8254819078de64977f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752831"
---
# <a name="iwiaimagefiltersetnewcallback-method"></a>Metodo IWiaImageFilter:: SetNewCallback

Imposta un nuovo callback dell'applicazione per il filtro di elaborazione dell'immagine da utilizzare per l'invio delle chiamate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNewCallback(
  [in] IWiaTransferCallback pWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaTransferCallback* \[ in\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)**

Specifica un puntatore all'interfaccia [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Non chiamare questo metodo direttamente dall'applicazione.

Il filtro di elaborazione delle immagini è necessario per rilasciare l'interfaccia di callback dell'applicazione precedentemente archiviata prima di impostare il nuovo callback.

Se *pWiaTransferCallback* è **null**, il filtro di elaborazione dell'immagine deve semplicemente rilasciare il callback precedente dell'applicazione e restituire S \_ OK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




