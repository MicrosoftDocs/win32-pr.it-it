---
description: Invia un comando a un dispositivo hardware Windows Image Acquisition (WIA) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: Metodo IWiaItem2::D eviceCommand (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307366"
---
# <a name="iwiaitem2devicecommand-method"></a>IWiaItem2::D Metodo eviceCommand

Invia un comando a un dispositivo hardware Windows Image Acquisition (WIA) 2,0.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*pCmdGUID* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

Specifica il comando da inviare al dispositivo WIA 2,0. Vedere [_ *comandi* * del dispositivo WIA](-wia-wia-device-commands.md).

</dd> <dt>

*ppIWiaItem2* \[ in uscita\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore all'elemento [**IWiaItem2**](-wia-iwiaitem2.md) creato dal comando, se disponibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Oltre ai codici di errore COM standard, il metodo può restituire il valore seguente.



| Codice restituito                                                                                       | Descrizione                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | Il comando non è implementato per l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) in cui viene chiamato il metodo. Il valore numerico per questo errore non è ancora definito. <br/> |



 

## <a name="remarks"></a>Commenti

Il comportamento di questo metodo è diverso a seconda della categoria del nodo in cui viene chiamato il metodo.

Quando l'applicazione invia il comando [**WIA \_ cmd \_ Take \_ Picture**](-wia-wia-device-commands.md) al dispositivo usando il metodo **IWiaItem2::D EVICECOMMAND** , il sistema di runtime WIA 2,0 crea un oggetto [**IWiaItem2**](-wia-iwiaitem2.md) per rappresentare l'immagine. Il metodo **IWiaItem2::D evicecommand** archivia l'indirizzo dell'interfaccia nel parametro *ppIWiaItem2* .

Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
