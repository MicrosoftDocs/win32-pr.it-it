---
description: Rimuove l'oggetto IWiaItem2 corrente dalla struttura ad albero di oggetti del dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: Metodo IWiaItem2::D eleteItem (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeleteItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ef6a4204b591f06811f0941ca0ceed72b76151db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307367"
---
# <a name="iwiaitem2deleteitem-method"></a>IWiaItem2::D Metodo eleteItem

Rimuove l'oggetto [**IWiaItem2**](-wia-iwiaitem2.md) corrente dalla struttura ad albero di oggetti del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il sistema di runtime Windows Image Acquisition (WIA) 2,0 rappresenta ogni dispositivo hardware WIA 2,0 connesso al computer dell'utente come albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) . Un dispositivo WIA 2,0 specificato può o meno consentire alle applicazioni di eliminare oggetti **IWiaItem2** dal relativo albero. Gli elementi con elementi figlio non possono essere eliminati. Per eseguire una query sul dispositivo per la funzionalità di eliminazione degli elementi, è necessario usare l'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .

Se il dispositivo supporta l'eliminazione di elementi nella struttura ad albero di [**IWiaItem2**](-wia-iwiaitem2.md) , chiamare il metodo **IWiaItem2::D eleteitem** per rimuovere l'oggetto **IWiaItem2** . Si noti che questo metodo elimina un oggetto solo dopo che tutti i riferimenti all'oggetto sono stati rilasciati. Se l'eliminazione di un elemento non è riuscita, \_ viene restituito E DeleteItem. Il valore numerico per questo errore non è ancora definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




