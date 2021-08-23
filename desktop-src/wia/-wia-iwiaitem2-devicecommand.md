---
description: Elava un comando per un Windows hardware WIA (Image Acquisition) 2.0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: Metodo IWiaItem2::D eviceCommand (Wia.h)
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
ms.openlocfilehash: f70fd7b4a987dac3a079651f2cbc04dc50817ba8a43f8da1449a3f605683ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706311"
---
# <a name="iwiaitem2devicecommand-method"></a>Metodo IWiaItem2::D eviceCommand

Elava un comando per un Windows hardware WIA (Image Acquisition) 2.0.

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

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*pCmdGUID* \[ Pollici\]
</dt> <dd>

Tipo: **CONST \* GUID**

Specifica il comando da inviare al dispositivo WIA 2.0. Vedere [**Comandi del dispositivo WIA.**](-wia-wia-device-commands.md)

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore [**all'elemento IWiaItem2**](-wia-iwiaitem2.md) creato dal comando, se presente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Oltre ai codici di errore COM standard, il metodo può restituire il valore seguente.



| Codice restituito                                                                                       | Descrizione                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ CMDNOTSUPPORTED**</dt> </dl> | Il comando non è implementato per [**l'interfaccia IWiaItem2**](-wia-iwiaitem2.md) su cui viene chiamato il metodo . Il valore numerico per questo errore non è ancora definito. <br/> |



 

## <a name="remarks"></a>Commenti

Il comportamento di questo metodo è diverso a seconda della categoria del nodo in cui viene chiamato il metodo.

Quando l'applicazione invia il comando [**\_ WIA CMD \_ TAKE \_ PICTURE**](-wia-wia-device-commands.md) al dispositivo usando il metodo **IWiaItem2::D eviceCommand,** il sistema di run-time WIA 2.0 crea un [**oggetto IWiaItem2**](-wia-iwiaitem2.md) per rappresentare l'immagine. Il **metodo IWiaItem2::D eviceCommand** archivia l'indirizzo dell'interfaccia nel *parametro ppIWiaItem2.*

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppIWiaItem2.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
