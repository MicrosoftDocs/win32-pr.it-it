---
description: "Metodo IWiaDevMgr2::SelectDeviceDlgID: visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine."
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: Metodo IWiaDevMgr2::SelectDeviceDlgID (Wia.h)
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
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106819"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>Metodo IWiaDevMgr2::SelectDeviceDlgID

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

*hwndParent* \[ Pollici\]
</dt> <dd>

Tipo: **HWND**

Specifica la finestra padre della finestra **di dialogo Seleziona** dispositivo.

</dd> <dt>

*lDeviceType* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica il tipo di dispositivo WIA 2.0 da usare. Per un elenco dei valori possibili, vedere Identificatori di tipo di dispositivo [WIA.](-wia-wia-device-type-specifiers.md)

</dd> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica il comportamento della finestra di dialogo. Il valore può essere uno dei seguenti.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Usare il comportamento predefinito

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ DEVICE \_ NODEFAULT**


</dt> <dd>

Visualizzare la finestra di dialogo anche se è presente un solo dispositivo corrispondente.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Tipo: **BSTR \***

Puntatore a una stringa che riceve la stringa dell'identificatore del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                  | Descrizione                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Il dispositivo è stato selezionato correttamente. <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | L'utente ha annullato la finestra di dialogo. <br/>                                                              |
| <dl> <dt>**WIA S NO DEVICE AVAILABLE (WIA \_ S \_ NESSUN DISPOSITIVO \_ \_ DISPONIBILE)**</dt> </dl> | Nessun dispositivo hardware WIA 2.0 corrisponde alle specifiche fornite nel *parametro lDeviceType.* <br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea e visualizza la finestra **di dialogo Seleziona** dispositivo in modo che l'utente possa selezionare un dispositivo WIA 2.0 per l'acquisizione dell'immagine. Se un dispositivo viene selezionato correttamente, il metodo **IWiaDevMgr2::SelectDeviceDlgID** passa la stringa dell'identificatore all'applicazione tramite il relativo *parametro pbstrDeviceID.*

L'applicazione può limitare i dispositivi visualizzati all'utente a tipi specifici specificando i tipi di dispositivo tramite il *parametro lDeviceType.* Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2::SelectDeviceDlgID** non visualizza la **finestra di dialogo** Seleziona dispositivo. Passa invece la stringa dell'identificatore del dispositivo all'applicazione senza visualizzare la finestra di dialogo. È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2::SelectDeviceDlgID** per visualizzare la finestra di dialogo passando WIA SELECT DEVICE NODEFAULT come valore per il \_ \_ parametro \_ *lFlags.* Se più di un dispositivo WIA 2.0 corrisponde alla specifica, tutti i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo Seleziona dispositivo in modo che l'utente possa sceglierne uno.

> [!Note]  
> È consigliabile che le applicazioni rendono disponibile la selezione di dispositivi e immagini tramite una voce di menu denominata **Da scanner** nel menu **File.**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows Vista \[\]<br/>                                     |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




