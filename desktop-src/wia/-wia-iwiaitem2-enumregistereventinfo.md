---
description: "Il metodo IWiaItem2:: EnumRegisterEventInfo crea un enumeratore che è possibile usare per ottenere informazioni sugli eventi per i quali è stata registrata un'applicazione."
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'Metodo IWiaItem2:: EnumRegisterEventInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129427"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>Metodo IWiaItem2:: EnumRegisterEventInfo

Il metodo **IWiaItem2:: EnumRegisterEventInfo** crea un enumeratore che è possibile usare per ottenere informazioni sugli eventi per i quali è stata registrata un'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Non usato. Impostare su 0.

</dd> <dt>

*pEventGUID* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Puntatore a un identificatore che specifica l'evento hardware per il quale si desidera ottenere le informazioni di registrazione.

</dd> <dt>

_ppIEnum * \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Indirizzo di un puntatore all'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Un'applicazione chiama questo metodo per creare un oggetto enumeratore per le informazioni sull'evento. **IWiaItem2:: EnumRegisterEventInfo** archivia l'indirizzo dell'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) dell'oggetto enumeratore nel parametro *ppIEnum* . Il programma usa quindi il puntatore di interfaccia per enumerare le proprietà dell'evento per cui è registrato.

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnum* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
