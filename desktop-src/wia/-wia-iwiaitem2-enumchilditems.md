---
description: Crea un oggetto enumeratore e passa di nuovo un puntatore alla relativa interfaccia IEnumWiaItem2 per le cartelle con elementi nell'albero IWiaItem2 di un dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'Metodo IWiaItem2:: EnumChildItems (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485068"
---
# <a name="iwiaitem2enumchilditems-method"></a>Metodo IWiaItem2:: EnumChildItems

Crea un oggetto enumeratore e passa di nuovo un puntatore alla relativa interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) per le cartelle con elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) di un dispositivo Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCategoryGUID* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Specifica un puntatore a una categoria per cui vengono enumerati i nodi figlio. Se _ * NULL * *, vengono enumerati tutti i nodi figlio.

</dd> <dt>

*ppIEnumWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) creata da questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Il sistema di runtime WIA 2,0 rappresenta ogni dispositivo hardware WIA 2,0 come albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) . Il metodo **IWiaItem2:: EnumChildItems** consente alle applicazioni di enumerare gli elementi figlio nell'elemento corrente. Tuttavia, può essere applicato solo a elementi che sono cartelle.

Se la cartella non è vuota, contiene un sottoalbero di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) . Il metodo **IWiaItem2:: EnumChildItems** enumera tutti gli elementi contenuti nella cartella. Archivia un puntatore a un enumeratore nel parametro *ppIEnumWiaItem2* . Le applicazioni utilizzano il puntatore dell'enumeratore per eseguire l'enumerazione degli elementi figlio di un oggetto.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnumWiaItem2* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
