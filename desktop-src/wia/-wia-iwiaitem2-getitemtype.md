---
description: Ottiene le informazioni sul tipo di un elemento.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'Metodo IWiaItem2:: GetItemType (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751783"
---
# <a name="iwiaitem2getitemtype-method"></a>Metodo IWiaItem2:: GetItemType

Ottiene le informazioni sul tipo di un elemento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pItemType* \[ out\]
</dt> <dd>

Tipo: **Long \** _

Riceve un puntatore a un oggetto _ *Long** che contiene una combinazione di flag di tipo. Vedere i [**flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Ogni oggetto [**IWiaItem2**](-wia-iwiaitem2.md) nell'albero gerarchico di oggetti associati a un dispositivo hardware Windows Image Acquisition (WIA) 2,0 dispone di un tipo di dati specifico. Gli oggetti Item rappresentano cartelle e file. Le cartelle contengono oggetti file. Gli oggetti file contengono i dati acquisiti dal dispositivo, ad esempio immagini e suoni. Questo metodo consente alle applicazioni di identificare il tipo di qualsiasi elemento in un albero gerarchico di oggetti elemento in un dispositivo.

Un elemento può avere più di un tipo. Ad esempio, un elemento che rappresenta un file audio avrà gli attributi di tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




