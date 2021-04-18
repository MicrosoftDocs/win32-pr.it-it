---
description: Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'Metodo IWiaDevMgr2:: SelectDeviceDlgID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308233"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>Metodo IWiaDevMgr2:: SelectDeviceDlgID

Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Tipo: **HWND**

Consente di specificare la finestra padre della finestra di dialogo **Seleziona dispositivo** .

</dd> <dt>

*lDeviceType* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il tipo di dispositivo WIA 2,0 da usare. Per un elenco di valori possibili, vedere gli [identificatori del tipo di dispositivo WIA](-wia-wia-device-type-specifiers.md) .

</dd> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il comportamento della finestra di dialogo. Il valore può essere uno dei seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Usare il comportamento predefinito

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selezionare il \_ dispositivo \_ NODEFAULT**


</dt> <dd>

Visualizzare la finestra di dialogo anche se è presente un solo dispositivo corrispondente.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Tipo: **BSTR \** _

Puntatore a una stringa che riceve la stringa dell'identificatore del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                  | Descrizione                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                         | La selezione del dispositivo è stata completata. <br/>                                                          |
| <dl> <dt>**S \_ false**</dt> </dl>                      | L'utente ha annullato la finestra di dialogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ nessun \_ dispositivo \_ disponibile**</dt> </dl> | Nessun dispositivo hardware WIA 2,0 corrisponde alle specifiche specificate nel parametro *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea e visualizza la finestra di dialogo **Seleziona dispositivo** in modo che l'utente possa selezionare un dispositivo WIA 2,0 per l'acquisizione dell'immagine. Se un dispositivo viene selezionato correttamente, il metodo **IWiaDevMgr2:: SelectDeviceDlgID** passa la stringa dell'identificatore all'applicazione tramite il parametro *pbstrDeviceID* .

L'applicazione può limitare i dispositivi visualizzati all'utente a determinati tipi specificando i tipi di dispositivo tramite il parametro *lDeviceType* . Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2:: SelectDeviceDlgID** non Visualizza la finestra di dialogo **Seleziona dispositivo** . Passa invece la stringa dell'identificatore del dispositivo all'applicazione senza visualizzare la finestra di dialogo. È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2:: SelectDeviceDlgID** per visualizzare la finestra di dialogo passando WIA \_ Select \_ Device \_ NODEFAULT come valore per il parametro *è* . Se più di un dispositivo WIA 2,0 corrisponde alla specifica, tutti i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo SelectDevice in modo che l'utente possa sceglierne uno.

> [!Note]  
> È consigliabile che le applicazioni rendano disponibili la selezione del dispositivo e dell'immagine tramite una voce di menu denominata **da scanner** nel menu **file** .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




