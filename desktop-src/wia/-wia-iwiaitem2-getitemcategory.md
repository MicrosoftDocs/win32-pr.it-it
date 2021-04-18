---
description: Ottiene le informazioni sulla categoria di un elemento.
ms.assetid: 4d6f7a6a-280d-4b36-8e1d-8d9fcaa8a1de
title: 'Metodo IWiaItem2:: GetItemCategory (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemCategory
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: fdf650e8b540fcb9dc58f93f34771462fbc0a5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307362"
---
# <a name="iwiaitem2getitemcategory-method"></a>Metodo IWiaItem2:: GetItemCategory

Ottiene le informazioni sulla categoria di un elemento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetItemCategory(
  [out] GUID *pItemCategoryGUID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pItemCategoryGUID* \[ out\]
</dt> <dd>

Tipo: **GUID \** _

Riceve un puntatore al GUID che identifica la categoria dell'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Ogni oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero gerarchico di oggetti associati a un dispositivo hardware Windows Image Acquisition (WIA) 2,0 dispone di una categoria specifica. Questo metodo consente alle applicazioni di identificare la categoria di qualsiasi elemento in un albero gerarchico di oggetti elemento in un dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




