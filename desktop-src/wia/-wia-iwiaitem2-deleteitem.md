---
description: Rimuove l'oggetto IWiaItem2 corrente dall'albero di oggetti del dispositivo.
ms.assetid: 247eb36f-3e5c-4030-8334-1a4028b3eb44
title: Metodo IWiaItem2::D eleteItem (Wia.h)
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
ms.openlocfilehash: 791d596ee48c4d3e2efd67259ec2e37249c930c6da32f704d332df1da6930503
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593001"
---
# <a name="iwiaitem2deleteitem-method"></a>Metodo IWiaItem2::D eleteItem

Rimuove [**l'oggetto IWiaItem2 corrente**](-wia-iwiaitem2.md) dall'albero di oggetti del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeleteItem(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Il sistema di run-time di Windows Image Acquisition (WIA) 2.0 rappresenta ogni dispositivo hardware WIA 2.0 connesso al computer dell'utente come albero gerarchico di oggetti [**IWiaItem2.**](-wia-iwiaitem2.md) Un determinato dispositivo WIA 2.0 può consentire o meno alle applicazioni di eliminare oggetti **IWiaItem2** dal relativo albero. Gli elementi con elementi figlio non possono essere eliminati. [**L'interfaccia IEnumWIA \_ DEV \_ CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) deve essere usata per eseguire query sul dispositivo per la funzionalità di eliminazione degli elementi.

Se il dispositivo supporta l'eliminazione di elementi nell'albero [**IWiaItem2,**](-wia-iwiaitem2.md) chiamare il metodo **IWiaItem2::D eleteItem** per rimuovere **l'oggetto IWiaItem2.** Si noti che questo metodo elimina un oggetto solo dopo il rilascio di tutti i riferimenti all'oggetto. Se l'eliminazione di un elemento non è riuscita, viene restituito E \_ DELETEITEM. Il valore numerico per questo errore non è ancora definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




