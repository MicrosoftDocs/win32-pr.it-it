---
description: Inizializza il filtro. Chiamato da Windows Image Acquisition (WIA) 2,0 prima del download di ogni immagine.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'Metodo IWiaImageFilter:: InitializeFilter (WIA. h)'
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
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312398"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>Metodo IWiaImageFilter:: InitializeFilter

Inizializza il filtro. Chiamato da Windows Image Acquisition (WIA) 2,0 prima del download di ogni immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWiaItem2* \[ in\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Specifica un puntatore all'elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) che rappresenta l'immagine di anteprima.

</dd> <dt>

*pWiaTransferCallback* \[ in\]
</dt> <dd>

Tipo: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Specifica un puntatore all'interfaccia [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando un'applicazione chiama [**download**](-wia-iwiatransfer-download.md) e quando un'applicazione chiama la funzione del componente WIA 2,0 Preview `GetNewPreview` . **IWiaImageFilter:: InitializeFilter** archivia i riferimenti a *pWiaItem2* e *pWiaTransferCallback* per passare a queste funzioni. Questi due puntatori di interfaccia devono essere archiviati come variabili membro e [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve essere chiamato per ogni. I puntatori di interfaccia sono necessari anche nell'implementazione del filtro di [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) e [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante l'acquisizione dell'immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
