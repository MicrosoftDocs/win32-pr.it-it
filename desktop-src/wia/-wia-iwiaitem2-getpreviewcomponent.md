---
description: Ottiene il componente Windows Image Acquisition (WIA) 2,0 Preview.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'Metodo IWiaItem2:: GetPreviewComponent (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129422"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>Metodo IWiaItem2:: GetPreviewComponent

Ottiene il componente Windows Image Acquisition (WIA) 2,0 Preview.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Non usato. Impostare su 0.

</dd> <dt>

*ppWiaPreview* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Restituisce l'indirizzo di un puntatore all'interfaccia [**IWiaPreview**](-wia-iwiapreview.md) del componente di anteprima.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Usare questa funzione per restituire un puntatore all'indirizzo del componente WIA 2,0 Preview per qualsiasi oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero degli oggetti di un dispositivo hardware WIA 2,0.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppWiaPreview* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
