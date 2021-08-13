---
description: "Metodo IWiaDevMgr2::SelectDeviceDlg: visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine."
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: Metodo IWiaDevMgr2::SelectDeviceDlg (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 344b13ec05e6f1d06011b3555e5b455202e5848b5000e799540d9f7c3160653b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441236"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>Metodo IWiaDevMgr2::SelectDeviceDlg

Visualizza una finestra di dialogo che consente all'utente di selezionare un dispositivo hardware per l'acquisizione dell'immagine.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
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

*pbstrDeviceID* \[ in, out\]
</dt> <dd>

Tipo: **BSTR \***

Nell'output riceve una stringa che contiene la stringa dell'identificatore del dispositivo. In input, passare l'indirizzo di un puntatore se queste informazioni sono necessarie oppure **NULL** se non sono necessarie.

</dd> <dt>

*ppItemRoot* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore [**all'interfaccia IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice dell'albero gerarchico che rappresenta il dispositivo WIA 2.0 selezionato. Se non viene trovato alcun dispositivo, riceve **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                                  | Descrizione                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Il dispositivo è stato selezionato correttamente. <br/>                                                          |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | L'utente ha annullato la finestra di dialogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S NESSUN DISPOSITIVO \_ \_ \_ DISPONIBILE**</dt> </dl> | Nessun dispositivo hardware WIA 2.0 corrisponde alle specifiche fornite nel *parametro lDeviceType.* <br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo crea e visualizza la finestra **di** dialogo Seleziona dispositivo in modo che l'utente possa selezionare un dispositivo WIA 2.0 per l'acquisizione dell'immagine. Se un dispositivo viene selezionato correttamente, il **metodo IWiaDevMgr2::SelectDeviceDlg** crea un albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) per il dispositivo. Archivia un puntatore **all'interfaccia IWiaItem2** dell'elemento radice nel parametro *ppItemRoot*.

L'applicazione può limitare i dispositivi visualizzati all'utente a tipi specifici specificando i tipi di dispositivo tramite il *parametro lDeviceType.* Se solo un dispositivo soddisfa la specifica, **IWiaDevMgr2::SelectDeviceDlg** non visualizza la **finestra** di dialogo Seleziona dispositivo. Crea invece [**l'albero IWiaItem2**](-wia-iwiaitem2.md) per il dispositivo e archivia un puntatore **all'interfaccia IWiaItem2** dell'elemento radice nel *parametro ppItemRoot*. È possibile eseguire l'override di questo comportamento e forzare **IWiaDevMgr2::SelectDeviceDlg** a visualizzare la finestra di dialogo specificando WIA SELECT DEVICE NODEFAULT come valore per il \_ \_ parametro \_ *lFlags.* Se più dispositivi WIA 2.0 corrispondono alla specifica, tutti  i dispositivi corrispondenti vengono visualizzati nella finestra di dialogo Seleziona dispositivo in modo che l'utente possa sceglierne uno.

Le applicazioni devono chiamare [il metodo IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori a interfaccia ricevuti tramite il *parametro ppItemRoot.*

> [!Note]  
> È consigliabile che le applicazioni rendono disponibile la selezione di dispositivi e immagini tramite una voce di menu denominata **Da scanner** nel menu **File.**

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
